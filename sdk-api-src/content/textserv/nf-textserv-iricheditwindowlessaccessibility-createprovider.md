---
UID: NF:textserv.IRicheditWindowlessAccessibility.CreateProvider
title: IRicheditWindowlessAccessibility::CreateProvider (textserv.h)
author: windows-sdk-content
description: Obtains a Microsoft UI Automation provider object for the parent of a windowless rich edit control.
old-location: controls\iricheditwindowlessaccessibility_createprovider.htm
tech.root: Controls
ms.assetid: 660E8B3E-1372-458D-A6E0-B88B1E5A01B5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateProvider, CreateProvider method [Windows Controls], CreateProvider method [Windows Controls],IRicheditWindowlessAccessibility interface, IRicheditWindowlessAccessibility interface [Windows Controls],CreateProvider method, IRicheditWindowlessAccessibility.CreateProvider, IRicheditWindowlessAccessibility::CreateProvider, controls.iricheditwindowlessaccessibility_createprovider, textserv/IRicheditWindowlessAccessibility::CreateProvider
ms.topic: method
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRicheditWindowlessAccessibility.CreateProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRicheditWindowlessAccessibility::CreateProvider


## -description


Obtains a Microsoft UI Automation provider object for the parent of a windowless rich edit control.


## -parameters




### -param pSite

Type: <b>IRawElementProviderWindowlessSite*</b>

The ActiveX control site that hosts the windowless rich edit control.


### -param ppProvider

Type: <b>IRawElementProviderSimple**</b>

The UI Automation provider for the windowless rich edit control's parent.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/E58E9577-4004-4627-A0D6-CF8166C0C43F">IRicheditWindowlessAccessibility</a>
 

 

