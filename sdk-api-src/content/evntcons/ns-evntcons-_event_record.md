---
UID: NS:evntcons._EVENT_RECORD
title: "_EVENT_RECORD"
author: windows-sdk-content
description: Defines the layout of an event that ETW delivers.
old-location: etw\event_record.htm
old-project: etw
ms.assetid: e352c1a7-39a2-43e3-a723-5fc6a3921ee8
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PEVENT_RECORD, EVENT_RECORD, EVENT_RECORD structure [ETW], PCEVENT_RECORD, PEVENT_RECORD, PEVENT_RECORD structure pointer [ETW], _EVENT_RECORD, base.event_record, etw.event_record, relogger/EVENT_RECORD, relogger/PEVENT_RECORD"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntcons.h
req.include-header: Evntcons.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EVENT_RECORD, *PEVENT_RECORD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - EVENT_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EVENT_RECORD structure


## -description


The <b>EVENT_RECORD</b> structure defines the layout of an event that ETW delivers.


## -struct-fields




### -field EventHeader

Information about the event such as the time stamp for when it was written. For details, see the <a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a> structure.


### -field BufferContext

Defines information such as the session that logged the event. For details, see the <a href="https://msdn.microsoft.com/75577305-fb3f-40a2-8fe6-9cd82c3f4e69">ETW_BUFFER_CONTEXT</a> structure.


### -field ExtendedDataCount

The number of extended data structures in the <b>ExtendedData</b> member.


### -field UserDataLength

The size, in bytes, of the data in the <b>UserData</b> member.


### -field ExtendedData

One or more extended data items that ETW collects.  The extended data includes some items, such as the security identifier (SID) of the user that logged the event, only if the controller sets the <i>EnableProperty</i> parameter passed to the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> or <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function. The extended data includes other items, such as the related activity identifier and decoding information for trace logging, regardless whether the controller sets the <i>EnableProperty</i> parameter passed to  <b>EnableTraceEx</b> or <b>EnableTraceEx2</b>.  For details, see the <a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a> structure .


### -field UserData

Event specific data. To parse this data, see <a href="https://msdn.microsoft.com/8164b963-6232-42aa-b15e-071ac389dd27">Retrieving Event Data Using TDH</a>. If the <b>Flags</b> member of <a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a> contains  <b>EVENT_HEADER_FLAG_STRING_ONLY</b>, the data is a null-terminated Unicode string that you do not need TDH to parse.


### -field UserContext

Th context specified in the <b>Context</b> member of the <a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a> structure that is passed to the <a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function.


## -remarks



The <b>EVENT_RECORD</b> structure is passed to the consumer's implementation of the <a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a> callback .




## -see-also




<a href="https://msdn.microsoft.com/75577305-fb3f-40a2-8fe6-9cd82c3f4e69">ETW_BUFFER_CONTEXT</a>



<a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a>



<a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a>



<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a>



<a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>



<a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a>



<a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a>
 

 

