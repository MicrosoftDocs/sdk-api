---
UID: NC:winbase.PFE_EXPORT_FUNC
title: PFE_EXPORT_FUNC (winbase.h)
author: windows-sdk-content
description: An application-defined callback function used with ReadEncryptedFileRaw.
old-location: fs\exportcallback.htm
tech.root: FileIO
ms.assetid: 156948c9-d7b4-4491-bdb1-e1864a32caab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExportCallback, ExportCallback callback, ExportCallback callback function [Files], PFE_EXPORT_FUNC, PFE_EXPORT_FUNC callback function [Files], base.exportcallback, fs.exportcallback, winbase/ExportCallback, winbase/PFE_EXPORT_FUNC
ms.topic: callback
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinBase.h
api_name:
 - ExportCallback
 - PFE_EXPORT_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFE_EXPORT_FUNC callback function


## -description


An application-defined callback function used with 
    <a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>. The system calls 
    <b>ExportCallback</b> one or more times, each time with a block 
    of the encrypted file's data, until it has received all of the file data. 
    <b>ExportCallback</b> writes the encrypted file's data to 
    another storage media, usually for purposes of backing up the file.

The <b>PFE_EXPORT_FUNC</b> type defines a pointer to the callback function. 
    <b>ExportCallback</b> is a placeholder for the 
    application-defined function name.


## -parameters




### -param pbData [in]

A pointer to a block of the encrypted file's data to be backed up. This block of data is allocated by the 
      system.


### -param pvCallbackContext [in, optional]

A pointer to an application-defined and allocated context block. The application passes this pointer to 
      <a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>, and 
      <b>ReadEncryptedFileRaw</b> passes this pointer to the 
      callback function so that it can have access to application-specific data. This data can be a structure and can 
      contain any data the application needs, such as the handle to the file that contains the backup copy of the 
      encrypted file.


### -param ulLength [in]

The size of the data pointed to by the <i>pbData</i> parameter, in bytes.


## -returns



If the function succeeds, it must set the return value to <b>ERROR_SUCCESS</b>.

If the function fails, set the return value to a nonzero error code defined in WinError.h. For 
       example, if this function fails because an API that it calls fails, you can set the return value to the value 
       returned by <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for the failed API.




## -remarks



You can use the application-defined context block for internal tracking of information such as the file handle 
     and the current offset in the file.




## -see-also




<a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/4c951e44-15d8-43c8-bd3d-293a1ec9d444">ImportCallback</a>



<a href="https://msdn.microsoft.com/f792f38d-783e-4f39-a9d8-0c378d508d97">OpenEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/f44e291e-dbc6-4a44-92ba-92a81e043764">WriteEncryptedFileRaw</a>
 

 

