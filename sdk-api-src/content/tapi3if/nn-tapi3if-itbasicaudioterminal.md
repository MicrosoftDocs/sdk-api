---
UID: NN:tapi3if.ITBasicAudioTerminal
title: ITBasicAudioTerminal (tapi3if.h)
description: The ITBasicAudioTerminal interface provides methods that allow an application to control basic sound characteristics of terminal.
helpviewer_keywords: ["ITBasicAudioTerminal","ITBasicAudioTerminal interface [TAPI 2.2]","ITBasicAudioTerminal interface [TAPI 2.2]","described","_tapi3_itbasicaudioterminal","tapi3.itbasicaudioterminal","tapi3if/ITBasicAudioTerminal"]
old-location: tapi3\itbasicaudioterminal.htm
tech.root: tapi3
ms.assetid: 3e676a16-f3ce-433c-9941-8cdccdb01efd
ms.date: 12/05/2018
ms.keywords: ITBasicAudioTerminal, ITBasicAudioTerminal interface [TAPI 2.2], ITBasicAudioTerminal interface [TAPI 2.2],described, _tapi3_itbasicaudioterminal, tapi3.itbasicaudioterminal, tapi3if/ITBasicAudioTerminal
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
 - ITBasicAudioTerminal
 - tapi3if/ITBasicAudioTerminal
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
 - ITBasicAudioTerminal
---

# ITBasicAudioTerminal interface


## -description

The 
<b>ITBasicAudioTerminal</b> interface provides methods that allow an application to control basic sound characteristics of terminal. These methods are taken from the <b>IBasicAudio</b> interface in DirectShow. Please check the index for the Platform Software Development Kit (SDK) for additional information.

The 
<b>ITBasicAudioTerminal</b> interface can be obtained through <b>QueryInterface</b> from terminal objects that support this interface. For example, if the computer running Windows 2000 has a sound card, the addresses exposed by the H323 and IPCONF providers will enumerate, in their 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a> interface, two static terminals that support the 
<b>ITBasicAudioTerminal</b> interface: one for "audio record" and one for "audio playback."

## -inheritance

The <b>ITBasicAudioTerminal</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITBasicAudioTerminal</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
