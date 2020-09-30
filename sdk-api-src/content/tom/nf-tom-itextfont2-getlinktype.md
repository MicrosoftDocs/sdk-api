---
UID: NF:tom.ITextFont2.GetLinkType
title: ITextFont2::GetLinkType (tom.h)
description: Gets the link type.
helpviewer_keywords: ["GetLinkType","GetLinkType method [Windows Controls]","GetLinkType method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetLinkType method","ITextFont2.GetLinkType","ITextFont2::GetLinkType","controls.itextfont2_getlinktype","tom/ITextFont2::GetLinkType","tomAutoLinkEmail","tomAutoLinkPath","tomAutoLinkPhone","tomAutoLinkURL","tomClientLink","tomFriendlyLinkAddress","tomFriendlyLinkName","tomNoLink"]
old-location: controls\itextfont2_getlinktype.htm
tech.root: Controls
ms.assetid: 5405b2ce-52c9-4630-a091-3221820a4e0b
ms.date: 12/05/2018
ms.keywords: GetLinkType, GetLinkType method [Windows Controls], GetLinkType method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetLinkType method, ITextFont2.GetLinkType, ITextFont2::GetLinkType, controls.itextfont2_getlinktype, tom/ITextFont2::GetLinkType, tomAutoLinkEmail, tomAutoLinkPath, tomAutoLinkPhone, tomAutoLinkURL, tomClientLink, tomFriendlyLinkAddress, tomFriendlyLinkName, tomNoLink
req.header: tom.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextFont2::GetLinkType
 - tom/ITextFont2::GetLinkType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.GetLinkType
---

# ITextFont2::GetLinkType


## -description

Gets the link type.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The link type. It can be one of the following values.         


<a id="tomNoLink"></a>
<a id="tomnolink"></a>
<a id="TOMNOLINK"></a>


#### tomNoLink

<a id="tomClientLink"></a>
<a id="tomclientlink"></a>
<a id="TOMCLIENTLINK"></a>


#### tomClientLink

<a id="tomFriendlyLinkName"></a>
<a id="tomfriendlylinkname"></a>
<a id="TOMFRIENDLYLINKNAME"></a>


#### tomFriendlyLinkName

<a id="tomFriendlyLinkAddress"></a>
<a id="tomfriendlylinkaddress"></a>
<a id="TOMFRIENDLYLINKADDRESS"></a>


#### tomFriendlyLinkAddress

<a id="tomAutoLinkURL"></a>
<a id="tomautolinkurl"></a>
<a id="TOMAUTOLINKURL"></a>


#### tomAutoLinkURL

<a id="tomAutoLinkEmail"></a>
<a id="tomautolinkemail"></a>
<a id="TOMAUTOLINKEMAIL"></a>


#### tomAutoLinkEmail

<a id="tomAutoLinkPhone"></a>
<a id="tomautolinkphone"></a>
<a id="TOMAUTOLINKPHONE"></a>


#### tomAutoLinkPhone

<a id="tomAutoLinkPath"></a>
<a id="tomautolinkpath"></a>
<a id="TOMAUTOLINKPATH"></a>


#### tomAutoLinkPath

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>