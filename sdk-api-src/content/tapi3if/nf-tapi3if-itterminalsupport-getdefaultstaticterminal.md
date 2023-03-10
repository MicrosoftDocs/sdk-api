---
UID: NF:tapi3if.ITTerminalSupport.GetDefaultStaticTerminal
title: ITTerminalSupport::GetDefaultStaticTerminal (tapi3if.h)
description: The GetDefaultStaticTerminal method gets the default static terminal for the media type specified.
helpviewer_keywords: ["GetDefaultStaticTerminal","GetDefaultStaticTerminal method [TAPI 2.2]","GetDefaultStaticTerminal method [TAPI 2.2]","ITTerminalSupport interface","ITTerminalSupport interface [TAPI 2.2]","GetDefaultStaticTerminal method","ITTerminalSupport.GetDefaultStaticTerminal","ITTerminalSupport::GetDefaultStaticTerminal","_tapi3_itterminalsupport_getdefaultstaticterminal","tapi3.itterminalsupport_getdefaultstaticterminal","tapi3if/ITTerminalSupport::GetDefaultStaticTerminal"]
old-location: tapi3\itterminalsupport_getdefaultstaticterminal.htm
tech.root: tapi3
ms.assetid: aad3a566-eb95-402c-b26f-da6bd89e52ea
ms.date: 12/05/2018
ms.keywords: GetDefaultStaticTerminal, GetDefaultStaticTerminal method [TAPI 2.2], GetDefaultStaticTerminal method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],GetDefaultStaticTerminal method, ITTerminalSupport.GetDefaultStaticTerminal, ITTerminalSupport::GetDefaultStaticTerminal, _tapi3_itterminalsupport_getdefaultstaticterminal, tapi3.itterminalsupport_getdefaultstaticterminal, tapi3if/ITTerminalSupport::GetDefaultStaticTerminal
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminalSupport::GetDefaultStaticTerminal
 - tapi3if/ITTerminalSupport::GetDefaultStaticTerminal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport.GetDefaultStaticTerminal
---

# ITTerminalSupport::GetDefaultStaticTerminal


## -description

The 
<b>GetDefaultStaticTerminal</b> method gets the default static terminal for the 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> specified.

## -parameters

### -param lMediaType [in]

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a> of the required terminal.

### -param Direction [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor of the terminal direction.

### -param ppTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface. <b>NULL</b> if no terminal is available.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No terminal is available. *<i>ppTerminal</i> will be returned as <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not a valid media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to create the Terminal object.

</td>
</tr>
</table>

## -remarks

This method does not return dynamic terminals. For example, having a media type of TAPIMEDIATYPE_VIDEO and a terminal direction of TD_RENDER defines a dynamic terminal; this method will fail with those parameters.

The default static terminal returned by this method is one of the static terminals returned by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">ITTerminalSupport::EnumerateStaticTerminals</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals">ITTerminalSupport::get_StaticTerminals</a>. Usually, the default terminal is the one selected as "preferred device" in Control Panel's "Sounds and Multimedia Properties" applet.

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITTerminalSupport::GetDefaultStaticTerminal</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>



<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>