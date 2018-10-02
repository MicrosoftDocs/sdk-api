---
UID: NS:objidl.tagINTERFACEINFO
title: tagINTERFACEINFO
author: windows-sdk-content
description: Contains information about incoming calls.
old-location: com\interfaceinfo.htm
tech.root: com
ms.assetid: 5c2c07bf-1c15-4f21-baef-103837ea24d0
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPINTERFACEINFO, INTERFACEINFO, INTERFACEINFO structure [COM], LPINTERFACEINFO, LPINTERFACEINFO structure pointer [COM], _com_INTERFACEINFO, com.interfaceinfo, objidl/INTERFACEINFO, objidl/LPINTERFACEINFO, tagINTERFACEINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Objidl.h
api_name:
 - INTERFACEINFO
product: Windows
targetos: Windows
req.typenames: INTERFACEINFO, *LPINTERFACEINFO
req.redist: 
---

# tagINTERFACEINFO structure


## -description


Contains information about incoming calls.


## -struct-fields




### -field pUnk

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object.


### -field iid

The identifier of the requested interface.


### -field wMethod

The interface method.


## -see-also




<a href="https://msdn.microsoft.com/7e31b518-ef4f-4bdd-b5c7-e1b16383a5be">IMessageFilter::HandleInComingCall</a>
 

 

