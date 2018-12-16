---
UID: NS:mi._MI_Class
title: MI_Class
author: windows-sdk-content
description: Represents the schema of an instance.
old-location: wmi_v2\mi_class.htm
tech.root: wmi_v2
ms.assetid: 7f02e0fa-9e58-455d-9cf4-1d1244c44422
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Class, MI_Class structure [Windows Management Infrastructure (MI)], mi/MI_Class, wmi._mi_class, wmi_v2.mi_class
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Class
product: Windows
targetos: Windows
req.typenames: MI_Class
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Class structure


## -description


Represents the schema of an instance.


## -struct-fields




### -field ft

Pointer to <b>MI_Class</b> function table.


### -field classDecl

Pointer to the class declaration.


### -field namespaceName

The namespace name.


### -field serverName

The server name.


### -field reserved

Reserved for internal use.


## -remarks



The <b>MI_Class</b> object represents the schema of an instance.  Classes can be retrieved from the server, and instances can be queried for the <b>MI_Class</b> object.  Use the <b>MI_Class</b> APIs rather than navigating the structures themselves.



