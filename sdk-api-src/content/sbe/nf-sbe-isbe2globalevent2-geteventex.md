---
UID: NF:sbe.ISBE2GlobalEvent2.GetEventEx
title: ISBE2GlobalEvent2::GetEventEx
author: windows-sdk-content
description: Gets a global spanning event and its data from a Stream Buffer Source filter.
old-location: mstv\isbe2globalevent2_geteventex.htm
old-project: mstv
ms.assetid: 44c30d8a-d62b-4e0f-8ff9-a4159df6d724
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetEventEx, GetEventEx method [Microsoft TV Technologies], GetEventEx method [Microsoft TV Technologies],ISBE2GlobalEvent2 interface, ISBE2GlobalEvent2 interface [Microsoft TV Technologies],GetEventEx method, ISBE2GlobalEvent2.GetEventEx, ISBE2GlobalEvent2::GetEventEx, mstv.isbe2globalevent2_geteventex, sbe/ISBE2GlobalEvent2::GetEventEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2GlobalEvent2.GetEventEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2GlobalEvent2::GetEventEx


## -description


Gets a global spanning event and its data from a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter. 


## -parameters




### -param idEvt [in]

GUID identifying the event.


### -param param1 [in]

First event-specific parameter.


### -param param2 [in]

Second event-specific parameter.


### -param param3 [in]

Third event-specific parameter.


### -param param4 [in]

Fourth event-specific parameter.


### -param pSpanning [out]

Receives a flag indicating whether the event is a spanning event.


### -param pcb [in, out]

Pointer to a value specifying the buffer size. If the <i>pb</i> parameter is <b>NULL</b>, this parameter returns the required buffer size.


### -param pb [out]

Pointer to a buffer that receives the event data. If this parameter is <b>NULL</b>, the <i>pcb</i> parameter returns the required buffer size. The structure of the event data depends on the event type. For a list of event types, see the description of the <a href="https://msdn.microsoft.com/f1fc2b7c-3f60-4d03-9c75-9b9d9450ceef">ISBE2SpanningEvent::GetEvent</a> method.


### -param pStreamTime [out]

Stream time of last data sample that was read from the 
    file before the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d03b2f9d-560d-4357-9388-ed287f4cc8db">ISBE2GlobalEvent2</a>



<a href="https://msdn.microsoft.com/f1fc2b7c-3f60-4d03-9c75-9b9d9450ceef">ISBE2SpanningEvent::GetEvent</a>
 

 

