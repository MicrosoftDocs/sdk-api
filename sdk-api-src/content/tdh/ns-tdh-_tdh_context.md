---
UID: NS:tdh._TDH_CONTEXT
title: "_TDH_CONTEXT"
author: windows-sdk-content
description: Defines the additional information required to parse an event.
old-location: etw\tdh_context_struct.htm
old-project: etw
ms.assetid: 184df0af-3ac5-406f-a298-4f23826ad85e
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "*PTDH_CONTEXT, TDH_CONTEXT, TDH_CONTEXT structure [ETW], _TDH_CONTEXT, etw.tdh_context_struct, tdh.tdh_context_struct, tdh/TDH_CONTEXT"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TDH_CONTEXT
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TDH_CONTEXT structure


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
 

 

