---
UID: NS:tdh._TDH_CONTEXT
title: TDH_CONTEXT (tdh.h)
author: windows-sdk-content
description: Defines the additional information required to parse an event.
old-location: etw\tdh_context_struct.htm
tech.root: ETW
ms.assetid: 184df0af-3ac5-406f-a298-4f23826ad85e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTDH_CONTEXT, TDH_CONTEXT, TDH_CONTEXT structure [ETW], etw.tdh_context_struct, tdh.tdh_context_struct, tdh/TDH_CONTEXT"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - TDH_CONTEXT
product: Windows
targetos: Windows
req.typenames: TDH_CONTEXT
req.redist: 
---

# TDH_CONTEXT structure


## -description


Defines the additional information required to parse an event.
	
	


## -struct-fields




### -field ParameterValue

Context value cast to a ULONGLONG. The context value is determined by the context type specified in <b>ParameterType</b>. For example, if the context type is TDH_CONTEXT_WPP_TMFFILE, the context value is a Unicode string that contains the name of the .tmf file. 


### -field ParameterType

Context type. For a list of types, see the <a href="https://msdn.microsoft.com/7892f0d2-84f6-4543-b94e-8501e3911266">TDH_CONTEXT_TYPE</a> enumeration.


### -field ParameterSize

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/81542550-79aa-4d67-a472-ac3ee3a3ce63">TdhGetEventInformation</a>
 

 

