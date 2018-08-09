---
UID: NS:mi._MI_Instance
title: "_MI_Instance"
author: windows-sdk-content
description: This structure represents a CIM instance. This object should not be accessed directly. Instead, the MI_Instance_* functions should be used.
old-location: wmi_v2\mi_instance.htm
old-project: wmi_v2
ms.assetid: 3dce1817-7995-49e5-8cc0-ee9496665e5c
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Instance, MI_Instance structure [Windows Management Infrastructure (MI)], _MI_Instance, mi/MI_Instance, wmi._mi_instance, wmi_v2.mi_instance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MI_Instance
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Instance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_Instance structure


## -description


This structure represents a CIM instance. This object should not be accessed directly. Instead, the 
  <b>MI_Instance_*</b> functions should be used.


## -struct-fields




### -field ft

Pointer to the <a href="https://msdn.microsoft.com/a8cd93b7-c9e0-415e-811a-33826e38417f">MI_InstanceFT</a> function table.


### -field classDecl

The class declaration for this instance.


### -field serverName

Optional server name. Can be null.


### -field nameSpace

Optional namespace. Can be null.


### -field reserved

Reserved for internal use.

