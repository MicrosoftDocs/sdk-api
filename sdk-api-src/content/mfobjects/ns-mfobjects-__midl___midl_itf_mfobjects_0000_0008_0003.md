---
UID: NS:mfobjects.__MIDL___MIDL_itf_mfobjects_0000_0008_0003
title: "__MIDL___MIDL_itf_mfobjects_0000_0008_0003"
author: windows-sdk-content
description: Contains media type information for registering a Media Foundation transform (MFT).
old-location: mf\mft_register_type_info.htm
tech.root: medfound
ms.assetid: 1d26b9ee-545a-4e47-9a68-b9e567f0dec4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 1d26b9ee-545a-4e47-9a68-b9e567f0dec4, MFT_REGISTER_TYPE_INFO, MFT_REGISTER_TYPE_INFO structure [Media Foundation], _MFT_REGISTER_TYPE_INFO, __MIDL___MIDL_itf_mfobjects_0000_0008_0003, mf.mft_register_type_info, mfobjects/MFT_REGISTER_TYPE_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfobjects.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFT_REGISTER_TYPE_INFO
product: Windows
targetos: Windows
req.typenames: MFT_REGISTER_TYPE_INFO
req.redist: 
---

# __MIDL___MIDL_itf_mfobjects_0000_0008_0003 structure


## -description


Contains media type information for registering a Media Foundation transform (MFT).
        


## -struct-fields




### -field guidMajorType

The major media type. For a list of possible values, see <a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Major Media Types</a>.
          


### -field guidSubtype

The media subtype. For a list of possible values, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/c38a1194-e2d8-42ca-8581-4054171f6f44">Audio Subtype GUIDs</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7dfd85e6-936e-4b78-a2cb-a5d59153e1c4">Video Subtype GUIDs</a>
</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/a3bd2b3c-0b0b-4d64-99cc-6093c773f71c">MFTEnum</a>



<a href="https://msdn.microsoft.com/d1bac1c7-3f9b-46b7-bdf7-c32983c648ee">MFTGetInfo</a>



<a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

