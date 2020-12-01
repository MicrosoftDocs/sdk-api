---
UID: NC:wininet.GOPHER_ATTRIBUTE_ENUMERATOR
title: GOPHER_ATTRIBUTE_ENUMERATOR (wininet.h)
description: Prototype for a callback function that processes attribute information from a Gopher server.
helpviewer_keywords: ["GOPHER_ATTRIBUTE_ENUMERATOR","GOPHER_ATTRIBUTE_ENUMERATOR callback","GOPHER_ATTRIBUTE_ENUMERATOR callback function [WinINet]","GopherAttributeEnumerator","_inet_gopher_attribute_enumerator_prototype","wininet.gopherattributeenumerator","wininet/GOPHER_ATTRIBUTE_ENUMERATOR"]
old-location: wininet\gopherattributeenumerator.htm
tech.root: wininet
ms.assetid: 1a319d79-7866-4121-a80f-22e3bf983a0a
ms.date: 12/05/2018
ms.keywords: GOPHER_ATTRIBUTE_ENUMERATOR, GOPHER_ATTRIBUTE_ENUMERATOR callback, GOPHER_ATTRIBUTE_ENUMERATOR callback function [WinINet], GopherAttributeEnumerator, _inet_gopher_attribute_enumerator_prototype, wininet.gopherattributeenumerator, wininet/GOPHER_ATTRIBUTE_ENUMERATOR
req.header: wininet.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GOPHER_ATTRIBUTE_ENUMERATOR
 - wininet/GOPHER_ATTRIBUTE_ENUMERATOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wininet.h
api_name:
 - GOPHER_ATTRIBUTE_ENUMERATOR
---

# GOPHER_ATTRIBUTE_ENUMERATOR callback function


## -description

<p class="CCE_Message">[The <i>GopherAttributeEnumerator</i> function is available for use in the operating systems specified in the Requirements section.]

Prototype for a callback function that processes attribute information from a Gopher server. This callback function is installed by a call to the 
<a href="/windows/desktop/api/wininet/nf-wininet-gophergetattributea">GopherGetAttribute</a> function.

The <b>GOPHER_ATTRIBUTE_ENUMERATOR</b> type defines a pointer to this callback function. <i>GopherAttributeEnumerator</i> is a placeholder for the application-defined function name.

## -parameters

### -param lpAttributeInfo

Pointer to a  <a href="/windows/desktop/api/wininet/ns-wininet-gopher_attribute_type">GOPHER_ATTRIBUTE_TYPE</a> structure. The 
<i>lpBuffer</i> parameter of 
<a href="/windows/desktop/api/wininet/nf-wininet-gophergetattributea">GopherGetAttribute</a> is used for storing this structure. The 
<i>lpBuffer</i> size must be equal to or greater than the value of MIN_GOPHER_ATTRIBUTE_LENGTH.

### -param dwError

Error value. This parameter is NO_ERROR if the attribute was parsed and written to the buffer successfully. If a problem was encountered, an error value is returned.

## -returns

Return <b>TRUE</b> to continue the enumeration, or <b>FALSE</b> to stop it immediately. This function is primarily used for returning the results of a Gopher+ ASK item.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>