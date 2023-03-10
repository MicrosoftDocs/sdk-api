---
UID: NC:winbase.PFE_IMPORT_FUNC
title: PFE_IMPORT_FUNC (winbase.h)
description: An application-defined callback function used with WriteEncryptedFileRaw. The system calls ImportCallback one or more times, each time to retrieve a portion of a backup file's data.
helpviewer_keywords: ["ImportCallback","ImportCallback callback","ImportCallback callback function [Files]","PFE_IMPORT_FUNC","PFE_IMPORT_FUNC callback function [Files]","base.importcallback","fs.importcallback","winbase/ImportCallback","winbase/PFE_IMPORT_FUNC"]
old-location: fs\importcallback.htm
tech.root: fs
ms.assetid: 4c951e44-15d8-43c8-bd3d-293a1ec9d444
ms.date: 12/05/2018
ms.keywords: ImportCallback, ImportCallback callback, ImportCallback callback function [Files], PFE_IMPORT_FUNC, PFE_IMPORT_FUNC callback function [Files], base.importcallback, fs.importcallback, winbase/ImportCallback, winbase/PFE_IMPORT_FUNC
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFE_IMPORT_FUNC
 - winbase/PFE_IMPORT_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinBase.h
api_name:
 - ImportCallback
 - PFE_IMPORT_FUNC
---

# PFE_IMPORT_FUNC callback function


## -description

An application-defined callback function used with 
    <a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>. The system calls 
    <b>ImportCallback</b> one or more times, each time to retrieve a 
    portion of a backup file's data. 
    <b>ImportCallback</b> reads the data from a backup file 
    sequentially and restores the data, and  the system continues calling it until  it has read all of the backup file 
    data.

The <b>PFE_IMPORT_FUNC</b> type defines a pointer to this callback function. 
    <b>ImportCallback</b> is a placeholder for the 
    application-defined function name.

## -parameters

### -param pbData [in]

A pointer to a system-supplied buffer that will receive a block of data to be restored.

### -param pvCallbackContext [in, optional]

A pointer to an application-defined and allocated context block. The application passes this pointer to 
      <a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>, and it passes this 
      pointer to the callback function so that the callback function can have access to application-specific data. 
      This data can be a structure and can contain any data the application needs, such as the handle to the file that 
      contains the backup copy of the encrypted file.

### -param ulLength [in, out]

On function entry, this parameter specifies the length of the buffer the system has supplied. The callback 
       function must write no more than this many bytes to the buffer pointed to by the 
       <i>pbData</i> parameter.

On exit, the function must set this to the number of bytes of data written into the 
       <i>pbData</i>.

## -returns

If the function succeeds, it must set the return value to <b>ERROR_SUCCESS</b>, and set 
       the value pointed to by the <i>ulLength</i> parameter to the number of bytes copied into 
       <i>pbData</i>.

When the end of the backup file is reached, set <i>ulLength</i> to zero to tell the system 
       that the entire file has been processed.

If the function fails, set the return value to a nonzero error code defined in WinError.h. For 
       example, if this function fails because an API that it calls fails, you can set the return value to the value 
       returned by <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for the failed API.

## -remarks

The system calls the <b>ImportCallback</b> function until the 
     callback function indicates there is no more data to restore. To indicate that there is no more data to be 
     restored, set <i>*ulLength</i> to 0 and use a return code of 
     <b>ERROR_SUCCESS</b>. You can use the application-defined context block for internal tracking 
     of information such as the file handle and the current offset in the file.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/nc-winbase-pfe_export_func">ExportCallback</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa">OpenEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw">ReadEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>