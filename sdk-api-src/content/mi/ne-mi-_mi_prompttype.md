---
UID: NE:mi._MI_PromptType
title: "_MI_PromptType"
author: windows-sdk-content
description: Defines prompt types for the CIM extensions.
old-location: wmi_v2\mi_prompttype.htm
old-project: wmi_v2
ms.assetid: 183f40ed-214f-4468-8036-7753ae18575b
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_PROMPTTYPE_CRITICAL, MI_PROMPTTYPE_NORMAL, MI_PromptType, MI_PromptType enumeration [Windows Management Infrastructure (MI)], _MI_PromptType, mi/MI_PROMPTTYPE_CRITICAL, mi/MI_PROMPTTYPE_NORMAL, mi/MI_PromptType, wmi._mi_prompttype, wmi_v2.mi_prompttype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_PromptType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_PromptType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_PromptType enumeration


## -description


Defines prompt types for the CIM extensions.


## -enum-fields




### -field MI_PROMPTTYPE_NORMAL

A parameter of the  <a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a> function that specifies whether the prompt is a normal prompt such as "are you sure you want to delete this file?"


### -field MI_PROMPTTYPE_CRITICAL

A parameter of the <a href="https://msdn.microsoft.com/ef50a509-20a8-482c-b7b9-0dc1f0ab4ee0">MI_Context_PromptUser</a> function that specifies whether the prompt is a critical prompt, such as "are you sure you want to format your hard disk drive?"

