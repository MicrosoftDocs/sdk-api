---
UID: NF:wmsdkidl.IWMDRMReader.SetDRMProperty
title: IWMDRMReader::SetDRMProperty
author: windows-sdk-content
description: The SetDRMProperty method on the reader object is used to set a DRM property, such as the DRM_Rights property.
old-location: wmformat\iwmdrmreader_setdrmproperty.htm
old-project: wmformat
ms.assetid: 52f606c2-a746-488f-bbf7-0d0e54b89bf9
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMDRMReader interface [windows Media Format],SetDRMProperty method, IWMDRMReader.SetDRMProperty, IWMDRMReader::SetDRMProperty, IWMDRMReaderSetDRMProperty, SetDRMProperty, SetDRMProperty method [windows Media Format], SetDRMProperty method [windows Media Format],IWMDRMReader interface, wmformat.iwmdrmreader_setdrmproperty, wmsdkidl/IWMDRMReader::SetDRMProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMReader.SetDRMProperty
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMReader::SetDRMProperty


## -description


<p class="CCE_Message">[<b>SetDRMProperty</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>SetDRMProperty</b> method on the reader object is used to set a DRM property, such as the <a href="https://msdn.microsoft.com/fbf62e8d-069e-427b-9093-6c579cdaa96a">DRM_Rights</a> property.




## -parameters




### -param pwstrName [in]

Specifies the name of the property to set.


### -param dwType [in]

One member of the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type. The only supported value for this method is <b>WMT_TYPE_STRING</b>.


### -param pValue [in]

Pointer to a byte array containing the attribute value.


### -param cbLength [in]

Size of <i>pValue</i>, in bytes.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/222ef91c-b776-4de8-b1ad-88c2beca05aa">DRM Attribute List</a>



<a href="https://msdn.microsoft.com/862fc8bc-6e40-4496-862a-c12c8a382116">DRM Properties</a>



<a href="https://msdn.microsoft.com/bf4ff0f3-1f78-43c4-be4d-c74209176e58">IWMDRMReader Interface</a>



<a href="https://msdn.microsoft.com/86ee18be-38a9-4f76-810c-e33281df8c23">IWMDRMReader::GetDRMProperty</a>



<a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a>
 

 

