---
UID: NS:objidl.tagSTATDATA
title: STATDATA (objidl.h)
description: Contains information used to specify each advisory connection.
helpviewer_keywords: ["*LPSTATDATA","LPSTATDATA","LPSTATDATA structure pointer [COM]","STATDATA","STATDATA structure [COM]","_ole_STATDATA","com.statdata","objidl/LPSTATDATA","objidl/STATDATA"]
old-location: com\statdata.htm
tech.root: com
ms.assetid: f31469b2-4a4a-4da5-9229-38ddd0bcc88e
ms.date: 12/05/2018
ms.keywords: '*LPSTATDATA, LPSTATDATA, LPSTATDATA structure pointer [COM], STATDATA, STATDATA structure [COM], _ole_STATDATA, com.statdata, objidl/LPSTATDATA, objidl/STATDATA'
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
targetos: Windows
req.typenames: STATDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTATDATA
 - objidl/tagSTATDATA
 - STATDATA
 - objidl/STATDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ObjIdl.h
api_name:
 - STATDATA
---

# STATDATA structure


## -description

Contains information used to specify each advisory connection. It is used for enumerating current advisory connections. It holds data returned by the <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> enumerator. This enumerator interface is returned by <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject:DAdvise</a>. Each advisory connection is specified by a unique <b>STATDATA</b> structure.

## -struct-fields

### -field formatetc

The <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure for the data of interest to the advise sink. The advise sink receives notification of changes to the data specified by this <b>FORMATETC</b> structure.

### -field advf

The <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a> enumeration value that determines when the advisory sink is notified of changes in the data.

### -field pAdvSink

The pointer for the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface that will receive change notifications.

### -field dwConnection

The token that uniquely identifies the advisory connection. This token is returned by the method that sets up the advisory connection.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>