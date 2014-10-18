#!/bin/bash
 
OUTDIR=~/Desktop/moby
BASE="/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS7.1.sdk/System/Library/Frameworks"
 
mkdir -p ${OUTDIR}
 
cd ${BASE}
for dir in *
do
  for file in `find $dir -name '*.h'`
  do
    echo "// ==========  ${file}" >> ${OUTDIR}/${dir}.h
    cat $file >> ${OUTDIR}/${dir}.h
  done
done
 
cat ${OUTDIR}/*.h > ${OUTDIR}/moby.h
