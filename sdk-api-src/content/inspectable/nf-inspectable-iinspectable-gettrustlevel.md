---
UID: NF:inspectable.IInspectable.GetTrustLevel
title: IInspectable::GetTrustLevel
author: windows-driver-content
description: Gets the trust level of the current Windows Runtime object.
old-location: winrt\iinspectable_gettrustlevel.htm
old-project: WinRT
ms.assetid: E7E8AFD1-A8B7-4023-9F8B-573E0D2622F6
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetTrustLevel, GetTrustLevel method [Windows Runtime], GetTrustLevel method [Windows Runtime],IInputPaneInterop interface, GetTrustLevel method [Windows Runtime],IInspectable interface, IInputPaneInterop interface [Windows Runtime],GetTrustLevel method, IInputPaneInterop::GetTrustLevel, IInspectable interface [Windows Runtime],GetTrustLevel method, IInspectable.GetTrustLevel, IInspectable::GetTrustLevel, inspectable/IInputPaneInterop::GetTrustLevel, inspectable/IInspectable::GetTrustLevel, winrt.iinspectable_gettrustlevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: inspectable.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inspectable.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TrustLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Inspectable.h
api_name:
-	IInspectable.GetTrustLevel
-	IInputPaneInterop.GetTrustLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInspectable::GetTrustLevel


## -description


Gets the trust level of the current Windows Runtime object.


## -parameters




### -param trustLevel [out]

Type: <b><a href="https://msdn.microsoft.com/75E30E4B-EE5F-41C4-AC22-91D542E920EB">TrustLevel</a>*</b>

The trust level of the current Windows Runtime object. The default is <b>BaseLevel</b>.


## -returns



Type: <b>HRESULT</b>

This method always returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/DAE4705C-B786-44D4-8B03-1523EFC4C190">IInputPaneInterop</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

