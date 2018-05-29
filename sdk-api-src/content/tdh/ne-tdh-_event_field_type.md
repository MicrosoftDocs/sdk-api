---
UID: NE:tdh._EVENT_FIELD_TYPE
title: "_EVENT_FIELD_TYPE"
author: windows-sdk-content
description: Defines the provider information to retrieve.
old-location: etw\event_field_type_enum.htm
old-project: ETW
ms.assetid: da525556-e42b-41cb-b954-300f378477e5
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: EVENT_FIELD_TYPE, EVENT_FIELD_TYPE enumeration [ETW], EventChannelInformation, EventInformationMax, EventKeywordInformation, EventLevelInformation, EventOpcodeInformation, EventTaskInformation, _EVENT_FIELD_TYPE, etw.event_field_type_enum, tdh.event_field_type_enum, tdh/EVENT_FIELD_TYPE, tdh/EventChannelInformation, tdh/EventInformationMax, tdh/EventKeywordInformation, tdh/EventLevelInformation, tdh/EventOpcodeInformation, tdh/EventTaskInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tdh.h
req.include-header: 
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
req.typenames: EVENT_FIELD_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tdh.h
api_name:
-	EVENT_FIELD_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _EVENT_FIELD_TYPE enumeration


## -description



		Defines the provider information to retrieve.


## -enum-fields




### -field EventKeywordInformation

Keyword information defined in the manifest. For providers that define themselves using MOF classes, this type returns the enable flags values if the provider class includes the Flags property. For details, see the "Specifying level and enable flags values for a provider" section of <a href="https://msdn.microsoft.com/3bc82074-05a7-411f-884f-5da1fd08112b">Event Tracing MOF Qualifiers</a>. 


### -field EventLevelInformation

Level information defined in the manifest.


### -field EventChannelInformation

Channel information defined in the manifest.


### -field EventTaskInformation

Task information defined in the manifest.


### -field EventOpcodeInformation

Operation code information defined in the manifest.


### -field EventInformationMax

Reserved.


## -remarks



If you specify <b>EventOpcodeInformation</b> when calling <a href="https://msdn.microsoft.com/ca3c1519-0b86-4bdb-b027-9c662df5466e">TdhQueryProviderFieldInformation</a>, you must specify the  <i>EventFieldValue</i> parameter as follows:

<ul>
<li>Bits 0 - 15 must contain the task value</li>
<li>Bits 16 - 23 must contain the opcode value</li>
</ul>
You can get the task and opcode values from <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_RECORD.EventHeader.EventDescriptor</a>.

WMI MOF class supports retrieving keyword and level information only.




## -see-also




<a href="https://msdn.microsoft.com/c3755ca2-7b17-4f86-9ae8-34621f8b8c1b">PROVIDER_FIELD_INFOARRAY</a>



<a href="https://msdn.microsoft.com/ab34a433-b641-4408-81d5-c93609204d24">TdhEnumerateProviderFieldInformation</a>



<a href="https://msdn.microsoft.com/ca3c1519-0b86-4bdb-b027-9c662df5466e">TdhQueryProviderFieldInformation</a>
 

 

