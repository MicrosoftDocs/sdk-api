---
UID: NE:winuser.tagINPUT_MESSAGE_ORIGIN_ID
title: INPUT_MESSAGE_ORIGIN_ID (winuser.h)

description: The ID of the input message source.
old-location: input_sourceid\input_message_origin_id.htm
tech.root: Input_SourceId
ms.assetid: 5637bf3a-9fd8-4c89-acd0-4e0e47c0a3bf

ms.date: 12/05/2018
ms.keywords: IMO_HARDWARE, IMO_INJECTED, IMO_SYSTEM, IMO_UNAVAILABLE, INPUT_MESSAGE_ORIGIN_ID, INPUT_MESSAGE_ORIGIN_ID enumeration, input_sourceid.input_message_origin_id, inputsourceid.input_message_origin_id, winuser/IMO_HARDWARE, winuser/IMO_INJECTED, winuser/IMO_SYSTEM, winuser/IMO_UNAVAILABLE, winuser/INPUT_MESSAGE_ORIGIN_ID
ms.topic: enum
f1_keywords: 
 - "winuser/INPUT_MESSAGE_ORIGIN_ID"
dev_langs:
 - c++
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - INPUT_MESSAGE_ORIGIN_ID
targetos: Windows
req.typenames: INPUT_MESSAGE_ORIGIN_ID
req.redist: 
ms.custom: 19H1
---

# INPUT_MESSAGE_ORIGIN_ID enumeration


## -description


The ID of the input message source.


## -enum-fields




### -field IMO_UNAVAILABLE

The source isn't identified.


### -field IMO_HARDWARE

The input message is from a hardware device or has been  injected into the message queue by an application that has the <b>UIAccess</b> attribute set to TRUE in its manifest file. 

For more information about the <b>UIAccess</b> attribute and application manifests, see <a href="/previous-versions/bb756883(v=msdn.10)">UAC References</a>.


### -field IMO_INJECTED

The input message has been injected (through the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> function) by an application that doesn't have the <b>UIAccess</b> attribute set to TRUE in its manifest file.


### -field IMO_SYSTEM

The system has injected the input message.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_sourceid/enumerations">Enumerations</a>
 

 

