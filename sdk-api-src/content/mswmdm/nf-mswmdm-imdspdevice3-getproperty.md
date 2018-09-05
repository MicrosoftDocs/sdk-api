---
UID: NF:mswmdm.IMDSPDevice3.GetProperty
title: IMDSPDevice3::GetProperty
author: windows-sdk-content
description: The GetProperty method retrieves a specific device property.
old-location: wmdm\imdspdevice3_getproperty.htm
old-project: WMDM
ms.assetid: e0665ba6-361d-488c-9100-68f39855b736
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetProperty, GetProperty method [windows Media Device Manager], GetProperty method [windows Media Device Manager],IMDSPDevice3 interface, IMDSPDevice3 interface [windows Media Device Manager],GetProperty method, IMDSPDevice3.GetProperty, IMDSPDevice3::GetProperty, IMDSPDevice3TransferSessionBegin, mswmdm/IMDSPDevice3::GetProperty, wmdm.imdspdevice3_getproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
 - IMDSPDevice3.GetProperty
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice3::GetProperty


## -description



The <b>GetProperty</b> method retrieves a specific device property.




## -parameters




### -param pwszPropName [in]

Name of property being retrieved from the device.


### -param pValue [out]

Returned value for the property.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The variant that <i>pValue</i> points to is set to an empty <b>PROPVARIANT</b>, that is, its VT is set to VT_EMPTY.

Service provider should set this variant to the appropriate property value for the property <i>pwszPropName</i>.

If <i>pwszPropName</i> is <b>g_wszWMDMSupportedDeviceProperties</b>, service provider should return an array of the supported device properties. In such case, the VT of variant should be VT_BSTR | VT_ARRAY.

For a list of standard device property names, see <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.

This method is similar to the <a href="https://msdn.microsoft.com/a341289b-79e6-4ac7-b0d3-72ad5953c1df">IMDSPStorage3::GetMetadata</a> and <a href="https://msdn.microsoft.com/0f7b3a68-97b3-4470-8ca8-e8eb8a5f83b7">IMDSPStorage4::GetSpecifiedMetadata</a> methods for storages, but this method can get only one property at a time.




## -see-also




<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/72bbf8c3-a7e1-4289-b5b0-a57f50d6f46e">IMDSPDevice3::SetProperty</a>



<a href="https://msdn.microsoft.com/a341289b-79e6-4ac7-b0d3-72ad5953c1df">IMDSPStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/0f7b3a68-97b3-4470-8ca8-e8eb8a5f83b7">IMDSPStorage4::GetSpecifiedMetadata</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>
 

 

