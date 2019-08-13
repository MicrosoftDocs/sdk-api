---
UID: NS:objidl.tagSTATDATA
title: STATDATA (objidl.h)
author: windows-sdk-content
description: Contains information used to specify each advisory connection.
old-location: com\statdata.htm
tech.root: com
ms.assetid: f31469b2-4a4a-4da5-9229-38ddd0bcc88e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSTATDATA, LPSTATDATA, LPSTATDATA structure pointer [COM], STATDATA, STATDATA structure [COM], _ole_STATDATA, com.statdata, objidl/LPSTATDATA, objidl/STATDATA"
ms.topic: struct
f1_keywords: 
 - "objidl/STATDATA"
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
ms.custom: 19H1
---

# STATDATA structure


## -description


Contains information used to specify each advisory connection. It is used for enumerating current advisory connections. It holds data returned by the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> enumerator. This enumerator interface is returned by <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject:DAdvise</a>. Each advisory connection is specified by a unique <b>STATDATA</b> structure.




## -struct-fields




### -field formatetc

The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure for the data of interest to the advise sink. The advise sink receives notification of changes to the data specified by this <b>FORMATETC</b> structure.


### -field advf

The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a> enumeration value that determines when the advisory sink is notified of changes in the data.


### -field pAdvSink

The pointer for the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface that will receive change notifications.


### -field dwConnection

The token that uniquely identifies the advisory connection. This token is returned by the method that sets up the advisory connection.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>
 

 

