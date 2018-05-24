---
UID: NE:mfobjects.__MIDL___MIDL_itf_mfobjects_0000_0017_0003
title: "__MIDL___MIDL_itf_mfobjects_0000_0017_0003"
author: windows-driver-content
description: Specifies the behavior when opening a file.
old-location: mf\mf_file_flags.htm
old-project: medfound
ms.assetid: 1e1c906e-c832-4df1-96f5-86e690c3c34e
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 1e1c906e-c832-4df1-96f5-86e690c3c34e, MF_FILEFLAGS_ALLOW_WRITE_SHARING, MF_FILEFLAGS_NOBUFFERING, MF_FILEFLAGS_NONE, MF_FILE_FLAGS, MF_FILE_FLAGS enumeration [Media Foundation], __MIDL___MIDL_itf_mfobjects_0000_0017_0003, mf.mf_file_flags, mfobjects/MF_FILEFLAGS_ALLOW_WRITE_SHARING, mfobjects/MF_FILEFLAGS_NOBUFFERING, mfobjects/MF_FILEFLAGS_NONE, mfobjects/MF_FILE_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfobjects.h
api_name:
-	MF_FILE_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mfobjects_0000_0017_0003 enumeration


## -description



          Specifies the behavior when opening a file.
        


## -enum-fields




### -field MF_FILEFLAGS_NONE


            Use the default behavior.
          


### -field MF_FILEFLAGS_NOBUFFERING


            Open the file with no system caching.
          


### -field MF_FILEFLAGS_ALLOW_WRITE_SHARING

Subsequent open operations can have write access to the file.



<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd">MFBeginCreateFile</a>



<a href="https://msdn.microsoft.com/29269ea4-151f-4819-ae49-9f1c13a901e5">MFCreateFile</a>



<a href="https://msdn.microsoft.com/1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678">MFCreateTempFile</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

