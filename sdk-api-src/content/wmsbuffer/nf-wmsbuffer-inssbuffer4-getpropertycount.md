---
UID: NF:wmsbuffer.INSSBuffer4.GetPropertyCount
title: INSSBuffer4::GetPropertyCount (wmsbuffer.h)
author: windows-sdk-content
description: The GetPropertyCount method retrieves the total number of buffer properties, also called data unit extensions, associated with the sample contained in the buffer object.
old-location: wmformat\inssbuffer4_getpropertycount.htm
tech.root: wmformat
ms.assetid: b47f26b3-e816-498d-adc3-c6d3357971e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPropertyCount, GetPropertyCount method [windows Media Format], GetPropertyCount method [windows Media Format],INSSBuffer4 interface, INSSBuffer4 interface [windows Media Format],GetPropertyCount method, INSSBuffer4.GetPropertyCount, INSSBuffer4::GetPropertyCount, INSSBuffer4GetPropertyCount, wmformat.inssbuffer4_getpropertycount, wmsbuffer/INSSBuffer4::GetPropertyCount
ms.topic: method
req.header: wmsbuffer.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - INSSBuffer4.GetPropertyCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INSSBuffer4::GetPropertyCount


## -description



The <b>GetPropertyCount</b> method retrieves the total number of buffer properties, also called data unit extensions, associated with the sample contained in the buffer object. When using <a href="https://msdn.microsoft.com/8812b7c9-610b-4c17-a274-55e043cfb091">INSSBuffer4::GetPropertyByIndex</a> to retrieve properties, the index used is between zero and the number specified by this method.




## -parameters




### -param pcBufferProperties [out]

Pointer to the size of buffer properties.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743256(v=VS.85).aspx">INSSBuffer4 Interface</a>
 

 

