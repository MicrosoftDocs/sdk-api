---
UID: NC:wabapi.WABOpen
title: WABOpen (wabapi.h)
author: windows-sdk-content
description: Do not use. Provides access to the address book through a number of object interfaces. The root interface is IAddrBook, which is a subset of the MAPI implementation of IAddrBook.
old-location: wab\_wab_WABOpen.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\functions\wabopen.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WABOpen, WABOpen callback, WABOpen callback function [Windows Address Book], _wab_WABOpen, wab._wab_WABOpen, wabapi/WABOpen
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


Do not use. Provides access to the address book through a number of object interfaces. The root interface is <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a>, which is a subset of the MAPI implementation of <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a>.


## -parameters




### -param lppAdrBook

Type: <b>LPADRBOOK*</b>

Address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a> interface returned by the function.


### -param lppWABObject

Type: <b>LPWABOBJECT*</b>

Address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms629467(v=VS.85).aspx">IWABObject</a> interface returned by the function.


### -param lpWP


### -param Reserved2

Type: <b>DWORD</b>

Reserved. Must be set to 0.


#### - lpWABParam

Type: <b>LPWAB_PARAM</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms629458(v=VS.85).aspx">WAB_PARAM</a> structure. Supported by Internet Explorer 4.0 or later.


## -returns



Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms629718(v=VS.85).aspx">WABOpenEx</a>
 

 

