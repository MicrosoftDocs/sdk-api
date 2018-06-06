---
UID: NE:mfobjects.__MIDL___MIDL_itf_mfobjects_0000_0017_0002
title: "__MIDL___MIDL_itf_mfobjects_0000_0017_0002"
author: windows-sdk-content
description: Specifies how to open or create a file.
old-location: mf\mf_file_openmode.htm
old-project: medfound
ms.assetid: 0c0e94fa-cbcc-4abc-9020-af6d36a4d3b6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 0c0e94fa-cbcc-4abc-9020-af6d36a4d3b6, MF_FILE_OPENMODE, MF_FILE_OPENMODE enumeration [Media Foundation], MF_OPENMODE_APPEND_IF_EXIST, MF_OPENMODE_DELETE_IF_EXIST, MF_OPENMODE_FAIL_IF_EXIST, MF_OPENMODE_FAIL_IF_NOT_EXIST, MF_OPENMODE_RESET_IF_EXIST, __MIDL___MIDL_itf_mfobjects_0000_0017_0002, mf.mf_file_openmode, mfobjects/MF_FILE_OPENMODE, mfobjects/MF_OPENMODE_APPEND_IF_EXIST, mfobjects/MF_OPENMODE_DELETE_IF_EXIST, mfobjects/MF_OPENMODE_FAIL_IF_EXIST, mfobjects/MF_OPENMODE_FAIL_IF_NOT_EXIST, mfobjects/MF_OPENMODE_RESET_IF_EXIST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_FILE_OPENMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_FILE_OPENMODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mfobjects_0000_0017_0002 enumeration


## -description



Specifies how to open or create a file.




## -enum-fields




### -field MF_OPENMODE_FAIL_IF_NOT_EXIST

Open an existing file. Fail if the file does not exist.


### -field MF_OPENMODE_FAIL_IF_EXIST

Create a new file. Fail if the file already exists.


### -field MF_OPENMODE_RESET_IF_EXIST

Open an existing file and truncate it, so that the size is zero bytes. Fail if the file does not already exist.


### -field MF_OPENMODE_APPEND_IF_EXIST

If the file does not exist, create a new file. If the file exists, open it.


### -field MF_OPENMODE_DELETE_IF_EXIST

Create a new file. If the file exists, overwrite the file.


## -see-also




<a href="https://msdn.microsoft.com/aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd">MFBeginCreateFile</a>



<a href="https://msdn.microsoft.com/29269ea4-151f-4819-ae49-9f1c13a901e5">MFCreateFile</a>



<a href="https://msdn.microsoft.com/1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678">MFCreateTempFile</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

