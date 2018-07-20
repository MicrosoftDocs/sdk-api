---
UID: NS:mfidl._MFT_REGISTRATION_INFO
title: "_MFT_REGISTRATION_INFO"
author: windows-sdk-content
description: Contains parameters for the IMFLocalMFTRegistration::RegisterMFTs method.
old-location: mf\mft_registration_info.htm
old-project: medfound
ms.assetid: 7d610edf-89e3-4ff3-9ad8-b92ee50df522
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: MFT_REGISTRATION_INFO, MFT_REGISTRATION_INFO structure [Media Foundation], _MFT_REGISTRATION_INFO, mf.mft_registration_info, mfidl/MFT_REGISTRATION_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MFT_REGISTRATION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFT_REGISTRATION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFT_REGISTRATION_INFO structure


## -description


Contains parameters for the <a href="https://msdn.microsoft.com/3f77b5b9-94af-42b1-83ca-cb3310083632">IMFLocalMFTRegistration::RegisterMFTs</a> method.


## -struct-fields




### -field clsid

CLSID of the Media Foundation transform (MFT) to register.


### -field guidCategory

GUID that specifies the category of the MFT. For a list of MFT categories, see <a href="https://msdn.microsoft.com/eca3ae3b-e40a-407d-986c-d0a85b891f52">MFT_CATEGORY</a>.


### -field uiFlags

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/ba39fb66-d8b6-49c1-8312-18ebdcb012c9">_MFT_ENUM_FLAG</a> enumeration.


### -field pszName

Wide-character string that contains the friendly name of the MFT.


### -field cInTypes

Number of elements in the <b>pInTypes</b> array.


### -field pInTypes

Pointer to an array of <a href="https://msdn.microsoft.com/1d26b9ee-545a-4e47-9a68-b9e567f0dec4">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array specifies an input format that the MFT supports. If this member is <b>NULL</b>, the <b>cInTypes</b> member must be zero.


### -field cOutTypes

Number of elements in the <b>pOutTypes</b> array.


### -field pOutTypes

Pointer to an array of <a href="https://msdn.microsoft.com/1d26b9ee-545a-4e47-9a68-b9e567f0dec4">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array defines an output format that the MFT supports. If this member is <b>NULL</b>, the <b>cOutTypes</b> member must be zero.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

