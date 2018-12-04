---
UID: NF:bits10_1.IBackgroundCopyCallback3.FileRangesTransferred
title: IBackgroundCopyCallback3::FileRangesTransferred
author: windows-sdk-content
description: BITS calls your implementation of the FileRangesTransferred method when one or more file ranges have been downloaded. File ranges are added to the job using the IBackgroundCopyFile6::RequestFileRanges method.
old-location: bits\ibackgroundcopycallback3_filerangestransferred.htm
tech.root: bits
ms.assetid: F47293D5-E21E-472A-AE62-4781D61D0430
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: FileRangesTransferred, FileRangesTransferred method [BITS], FileRangesTransferred method [BITS],IBackgroundCopyCallback3 interface, IBackgroundCopyCallback3 interface [BITS],FileRangesTransferred method, IBackgroundCopyCallback3.FileRangesTransferred, IBackgroundCopyCallback3::FileRangesTransferred, bits.ibackgroundcopycallback3_filerangestransferred, bits10_1/IBackgroundCopyCallback3::FileRangesTransferred
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyCallback3::FileRangesTransferred


## -description


BITS calls your implementation of the <b>FileRangesTransferred</b> method when one or more file ranges have been downloaded.  File ranges are added to the job using the <a href="https://msdn.microsoft.com/C36BDE94-03AC-4F06-B17B-B8729226F8AC">IBackgroundCopyFile6::RequestFileRanges</a> method.


## -parameters




### -param job

An <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> object that contains the  methods for accessing property, progress, and state information of the job. Do not release <i>pJob</i>; BITS releases the interface when the method returns.


### -param file

An <a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a> object that contains information about the file whose ranges have changed. Do not release <i>pFile</i>; BITS releases the interface when the method returns.


### -param rangeCount

The count of entries in the ranges array.


### -param ranges

An array of the files ranges that have transferred since the last call to <b>FileRangesTransferred</b>  or the last call to the <a href="https://msdn.microsoft.com/C36BDE94-03AC-4F06-B17B-B8729226F8AC">IBackgroundCopyFile6::RequestFileRanges</a> method. Do not free <i>ranges</i>; BITS frees the ranges memory when the <b>FileRangesTransferred</b> method returns. 


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

For an example of how to use this function, see the example code for the <a href="https://msdn.microsoft.com/74712770-BB14-4B8A-8DA4-096CEB58D820">IBackgroundCopyCallback3</a>interface.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/74712770-BB14-4B8A-8DA4-096CEB58D820">IBackgroundCopyCallback3</a>
 

 

