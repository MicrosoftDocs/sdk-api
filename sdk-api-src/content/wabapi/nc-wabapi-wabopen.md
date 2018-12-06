---
UID: NC:wabapi.WABOpen
title: WABOpen
author: windows-sdk-content
description: Do not use. Provides access to the address book through a number of object interfaces. The root interface is IAddrBook, which is a subset of the MAPI implementation of IAddrBook.
old-location: wab\_wab_WABOpen.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\functions\wabopen.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WABOpen, WABOpen callback, WABOpen callback function [Windows Address Book], _wab_WABOpen, wab._wab_WABOpen, wabapi/WABOpen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wabapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wabapi.h
api_name:
 - WABOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.5
---

# WABOpen callback function


## -description


Do not use. Provides access to the address book through a number of object interfaces. The root interface is <a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a>, which is a subset of the MAPI implementation of <a href="2681e3cf-a251-4c9d-9474-fc320fedede8">IAddrBook</a>.


## -parameters




### -param lppAdrBook

Type: <b>LPADRBOOK*</b>

Address of a pointer to the <a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a> interface returned by the function.


### -param lppWABObject

Type: <b>LPWABOBJECT*</b>

Address of a pointer to the <a href="https://msdn.microsoft.com/cba6a6ae-79e5-4412-9e1e-ad0ef41b1862">IWABObject</a> interface returned by the function.


### -param lpWP


### -param Reserved2

Type: <b>DWORD</b>

Reserved. Must be set to 0.


#### - lpWABParam

Type: <b>LPWAB_PARAM</b>

Pointer to a <a href="https://msdn.microsoft.com/0abed372-5972-4370-a3cb-d29d6aa68257">WAB_PARAM</a> structure. Supported by Internet Explorer 4.0 or later.


## -returns



Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8c4df4c8-c386-4e63-8cd4-2c8d6a4f69a7">WABOpenEx</a>
 

 

