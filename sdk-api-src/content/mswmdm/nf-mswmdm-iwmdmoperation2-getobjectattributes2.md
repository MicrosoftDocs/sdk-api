---
UID: NF:mswmdm.IWMDMOperation2.GetObjectAttributes2
title: IWMDMOperation2::GetObjectAttributes2
author: windows-driver-content
description: Windows Media Device Manager calls GetObjectAttributes when a file is written to the device in order to learn the attributes of the file.
old-location: wmdm\iwmdmoperation2_getobjectattributes2.htm
old-project: WMDM
ms.assetid: 7bf76094-5660-47ac-b1a2-a67b6f95964b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetObjectAttributes2, GetObjectAttributes2 method [windows Media Device Manager], GetObjectAttributes2 method [windows Media Device Manager],IWMDMOperation2 interface, IWMDMOperation2 interface [windows Media Device Manager],GetObjectAttributes2 method, IWMDMOperation2.GetObjectAttributes2, IWMDMOperation2::GetObjectAttributes2, IWMDMOperation2GetObjectAttributes2, mswmdm/IWMDMOperation2::GetObjectAttributes2, wmdm.iwmdmoperation2_getobjectattributes2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMOperation2.GetObjectAttributes2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMOperation2::GetObjectAttributes2


## -description



Windows Media Device Manager calls <b>GetObjectAttributes</b> when a file is written to the device in order to learn the attributes of the file.




## -parameters




### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> specifying the storage attributes defined in the <a href="https://msdn.microsoft.com/e43139d2-260a-4f27-a06c-aca741204663">IWMDMStorage::GetAttributes</a> method.


### -param pdwAttributesEx [out]

Pointer to a <b>DWORD</b> specifying extended attributes. There are currently no extended attributes defined.


### -param pAudioFormat [out]

Optional pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structure that specifies audio file attributes.


### -param pVideoFormat [out]

Optional pointer to a <a href="https://msdn.microsoft.com/5a39d66e-8dbc-4572-8370-14f722b6c906">_VIDEOINFOHEADER</a> structure that specifies video object attributes.


## -returns



The application should return one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The read operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The read operation should be cancelled without finishing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred, and the read operation should be cancelled without finishing.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b3f7e92a-8feb-47cd-ae50-bc5bf9a37958">IWMDMOperation2 Interface</a>



<a href="https://msdn.microsoft.com/ce19bfe5-c8ff-40f4-a152-8a46d2576c63">SetObjectAttributes2</a>
 

 

