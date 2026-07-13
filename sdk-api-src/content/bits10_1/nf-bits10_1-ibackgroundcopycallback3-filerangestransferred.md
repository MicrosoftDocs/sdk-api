---
UID: NF:bits10_1.IBackgroundCopyCallback3.FileRangesTransferred
title: IBackgroundCopyCallback3::FileRangesTransferred (bits10_1.h)
description: BITS calls your implementation of the FileRangesTransferred method when one or more file ranges have been downloaded. File ranges are added to the job using the IBackgroundCopyFile6::RequestFileRanges method.
helpviewer_keywords: ["FileRangesTransferred","FileRangesTransferred method [BITS]","FileRangesTransferred method [BITS]","IBackgroundCopyCallback3 interface","IBackgroundCopyCallback3 interface [BITS]","FileRangesTransferred method","IBackgroundCopyCallback3.FileRangesTransferred","IBackgroundCopyCallback3::FileRangesTransferred","bits.ibackgroundcopycallback3_filerangestransferred","bits10_1/IBackgroundCopyCallback3::FileRangesTransferred"]
old-location: bits\ibackgroundcopycallback3_filerangestransferred.htm
tech.root: Bits
ms.assetid: F47293D5-E21E-472A-AE62-4781D61D0430
ms.date: 12/05/2018
ms.keywords: FileRangesTransferred, FileRangesTransferred method [BITS], FileRangesTransferred method [BITS],IBackgroundCopyCallback3 interface, IBackgroundCopyCallback3 interface [BITS],FileRangesTransferred method, IBackgroundCopyCallback3.FileRangesTransferred, IBackgroundCopyCallback3::FileRangesTransferred, bits.ibackgroundcopycallback3_filerangestransferred, bits10_1/IBackgroundCopyCallback3::FileRangesTransferred
req.header: bits10_1.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback3::FileRangesTransferred
 - bits10_1/IBackgroundCopyCallback3::FileRangesTransferred
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyCallback3.FileRangesTransferred
---

# IBackgroundCopyCallback3::FileRangesTransferred


## -description

BITS calls your implementation of the <b>FileRangesTransferred</b> method when one or more file ranges have been downloaded.  File ranges are added to the job using the <a href="/windows/desktop/api/bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges">IBackgroundCopyFile6::RequestFileRanges</a> method.

## -parameters

### -param job

An <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> object that contains the  methods for accessing property, progress, and state information of the job. Do not release <i>pJob</i>; BITS releases the interface when the method returns.

### -param file

An <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> object that contains information about the file whose ranges have changed. Do not release <i>pFile</i>; BITS releases the interface when the method returns.

### -param rangeCount

The count of entries in the ranges array.

### -param ranges

An array of the files ranges that have transferred since the last call to <b>FileRangesTransferred</b>  or the last call to the <a href="/windows/desktop/api/bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges">IBackgroundCopyFile6::RequestFileRanges</a> method. Do not free <i>ranges</i>; BITS frees the ranges memory when the <b>FileRangesTransferred</b> method returns.

## -returns

This method returns <b>S_OK</b> on success; otherwise, returns an error code.

## -remarks

The ranges returned in this method may not match the ranges you requested.  This is because BITS will not download the same byte range twice, and because BITS can report when part of a range is downloaded.

Your implementation may not receive all modification events under maximum resource load conditions.

BITS generates a high volume of events; consider creating a timer and polling for state and progress information or limiting your use of this callback. If you use this callback, keep your implementation short.  You should set the <b>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL</b> property to the highest value that still meets your needs; this will reduce the number of unneeded callbacks.


<div class="alert"><b>Note</b>  BITS supports up to four simultaneous notifications per user. If one or more applications block all four notifications for a user from returning, an application running as the same user will not receive notifications until one or more of the blocking notifications return. 
</div>
<div> </div>

#### Examples

For an example of how to use this function, see the example code for the <a href="/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopycallback3">IBackgroundCopyCallback3</a> interface.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopycallback3">IBackgroundCopyCallback3</a>