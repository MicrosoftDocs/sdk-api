---
UID: NF:mswmdm.IWMDMOperation2.SetObjectAttributes2
title: IWMDMOperation2::SetObjectAttributes2
author: windows-sdk-content
description: The SetObjectAttributes2 method sets attributes of files or storages. This method is currently not called by Windows Media Device Manager.
old-location: wmdm\iwmdmoperation2_setobjectattributes2.htm
old-project: WMDM
ms.assetid: ce19bfe5-c8ff-40f4-a152-8a46d2576c63
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMOperation2 interface [windows Media Device Manager],SetObjectAttributes2 method, IWMDMOperation2.SetObjectAttributes2, IWMDMOperation2::SetObjectAttributes2, IWMDMOperation2SetObjectAttributes2, SetObjectAttributes2, SetObjectAttributes2 method [windows Media Device Manager], SetObjectAttributes2 method [windows Media Device Manager],IWMDMOperation2 interface, mswmdm/IWMDMOperation2::SetObjectAttributes2, wmdm.iwmdmoperation2_setobjectattributes2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMOperation2.SetObjectAttributes2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMOperation2::SetObjectAttributes2


## -description



The <b>SetObjectAttributes2</b> method sets attributes of files or storages. This method is currently not called by Windows Media Device Manager.




## -parameters




### -param dwAttributes [in]

Pointer to a <b>DWORD</b> specifying the attributes as defined by the <a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">IWMDMStorage::SetAttributes</a> method.


### -param dwAttributesEx [in]

<b>DWORD</b> specifying the extended attributes. No extended attributes are currently defined.


### -param pFormat [in]

Optional pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structure that specifies audio information about the object.


### -param pVideoFormat [in]

Optional pointer to a <a href="https://msdn.microsoft.com/5a39d66e-8dbc-4572-8370-14f722b6c906">_VIDEOINFOHEADER</a> structure that specifies video information about the object.


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




<a href="https://msdn.microsoft.com/7bf76094-5660-47ac-b1a2-a67b6f95964b">GetObjectAttributes2</a>



<a href="https://msdn.microsoft.com/b3f7e92a-8feb-47cd-ae50-bc5bf9a37958">IWMDMOperation2 Interface</a>
 

 

