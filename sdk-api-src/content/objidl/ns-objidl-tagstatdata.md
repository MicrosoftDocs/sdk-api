---
UID: NS:objidl.tagSTATDATA
title: tagSTATDATA
author: windows-sdk-content
description: Contains information used to specify each advisory connection.
old-location: com\statdata.htm
tech.root: com
ms.assetid: f31469b2-4a4a-4da5-9229-38ddd0bcc88e
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: "*LPSTATDATA, LPSTATDATA, LPSTATDATA structure pointer [COM], STATDATA, STATDATA structure [COM], _ole_STATDATA, com.statdata, objidl/LPSTATDATA, objidl/STATDATA, tagSTATDATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ObjIdl.h
api_name:
 - STATDATA
product: Windows
targetos: Windows
req.typenames: STATDATA
req.redist: 
---

# tagSTATDATA structure


## -description


Contains information used to specify each advisory connection. It is used for enumerating current advisory connections. It holds data returned by the <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> enumerator. This enumerator interface is returned by <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject:DAdvise</a>. Each advisory connection is specified by a unique <b>STATDATA</b> structure.




## -struct-fields




### -field formatetc

The <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure for the data of interest to the advise sink. The advise sink receives notification of changes to the data specified by this <b>FORMATETC</b> structure.


### -field advf

The <a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a> enumeration value that determines when the advisory sink is notified of changes in the data.


### -field pAdvSink

The pointer for the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface that will receive change notifications.


### -field dwConnection

The token that uniquely identifies the advisory connection. This token is returned by the method that sets up the advisory connection.



## -see-also




<a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>
 

 

