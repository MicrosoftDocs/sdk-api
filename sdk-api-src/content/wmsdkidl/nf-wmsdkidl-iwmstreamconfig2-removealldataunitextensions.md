---
UID: NF:wmsdkidl.IWMStreamConfig2.RemoveAllDataUnitExtensions
title: IWMStreamConfig2::RemoveAllDataUnitExtensions
author: windows-sdk-content
description: The RemoveAllDataUnitExtensions method removes all data unit extension systems that are associated with the stream.
old-location: wmformat\iwmstreamconfig2_removealldataunitextensions.htm
old-project: wmformat
ms.assetid: 944c1b6c-1d1b-4a44-9b9e-d673c8d60306
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMStreamConfig2 interface [windows Media Format],RemoveAllDataUnitExtensions method, IWMStreamConfig2.RemoveAllDataUnitExtensions, IWMStreamConfig2::RemoveAllDataUnitExtensions, IWMStreamConfig2RemoveAllDataUnitExtensions, RemoveAllDataUnitExtensions, RemoveAllDataUnitExtensions method [windows Media Format], RemoveAllDataUnitExtensions method [windows Media Format],IWMStreamConfig2 interface, wmformat.iwmstreamconfig2_removealldataunitextensions, wmsdkidl/IWMStreamConfig2::RemoveAllDataUnitExtensions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMStreamConfig2.RemoveAllDataUnitExtensions
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamConfig2::RemoveAllDataUnitExtensions


## -description



The <b>RemoveAllDataUnitExtensions</b> method removes all data unit extension systems that are associated with the stream.




## -parameters






## -returns



The method always returns S_OK.




## -remarks



The changes will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/db84a33c-bd83-46cb-a97c-76ddeeb74927">IWMStreamConfig2::AddDataUnitExtension</a>



<a href="https://msdn.microsoft.com/766124f6-b376-421b-b2ee-2c280af3bd16">IWMStreamConfig2::GetDataUnitExtension</a>



<a href="https://msdn.microsoft.com/f9a4ec84-4ea3-4e84-9def-7ca93be0f1ce">IWMStreamConfig2::GetDataUnitExtensionCount</a>
 

 

