---
UID: NN:tapi3if.IEnumTerminal
title: IEnumTerminal (tapi3if.h)
description: The IEnumTerminal interface provides COM-standard enumeration methods for the ITTerminal interface.
helpviewer_keywords: ["IEnumTerminal","IEnumTerminal interface [TAPI 2.2]","IEnumTerminal interface [TAPI 2.2]","described","_tapi3_ienumterminal","tapi3.ienumterminal","tapi3if/IEnumTerminal"]
old-location: tapi3\ienumterminal.htm
tech.root: tapi3
ms.assetid: a364e466-1d10-402f-935d-ff2713522fed
ms.date: 12/05/2018
ms.keywords: IEnumTerminal, IEnumTerminal interface [TAPI 2.2], IEnumTerminal interface [TAPI 2.2],described, _tapi3_ienumterminal, tapi3.ienumterminal, tapi3if/IEnumTerminal
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumTerminal
 - tapi3if/IEnumTerminal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumTerminal
---

# IEnumTerminal interface


## -description

The 
<b>IEnumTerminal</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface. The following methods return a pointer to 
<b>IEnumTerminal</b>:<dl>
<dd>
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-enumerateterminals">ITStream::EnumerateTerminals</a>
</dd>
<dd>
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-enumerateterminals">ITSubStream::EnumerateTerminals</a>
</dd>
<dd>
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">ITTerminalSupport::EnumerateStaticTerminals</a>
</dd>
</dl>


The 
<b>IEnumTerminal</b> interface is hidden from Visual Basic and scripting languages.

## -inheritance

The <b>IEnumTerminal</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTerminal</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
