---
UID: NE:oleidl.tagOLEUPDATE
title: OLEUPDATE (oleidl.h)
description: Indicates whether the linked object updates the cached data for the linked object automatically or only when the container calls either the IOleObject::Update or IOleLink::Update methods. The constants are used in the IOleLink interface.
helpviewer_keywords: ["*LPOLEUPDATE","*POLEUPDATE","LPOLEUPDATE","LPOLEUPDATE enumeration pointer [COM]","OLEUPDATE","OLEUPDATE enumeration [COM]","OLEUPDATE_ALWAYS","OLEUPDATE_ONCALL","POLEUPDATE","POLEUPDATE enumeration pointer [COM]","_ole_OLEUPDATE","com.oleupdate","oleidl/LPOLEUPDATE","oleidl/OLEUPDATE","oleidl/OLEUPDATE_ALWAYS","oleidl/OLEUPDATE_ONCALL","oleidl/POLEUPDATE"]
old-location: com\oleupdate.htm
tech.root: com
ms.assetid: 1945d4a2-dd1f-453e-ab7e-093f26171c84
ms.date: 12/05/2018
ms.keywords: '*LPOLEUPDATE, *POLEUPDATE, LPOLEUPDATE, LPOLEUPDATE enumeration pointer [COM], OLEUPDATE, OLEUPDATE enumeration [COM], OLEUPDATE_ALWAYS, OLEUPDATE_ONCALL, POLEUPDATE, POLEUPDATE enumeration pointer [COM], _ole_OLEUPDATE, com.oleupdate, oleidl/LPOLEUPDATE, oleidl/OLEUPDATE, oleidl/OLEUPDATE_ALWAYS, oleidl/OLEUPDATE_ONCALL, oleidl/POLEUPDATE'
req.header: oleidl.h
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
targetos: Windows
req.typenames: OLEUPDATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUPDATE
 - oleidl/tagOLEUPDATE
 - OLEUPDATE
 - oleidl/OLEUPDATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEUPDATE
---

# OLEUPDATE enumeration


## -description

Indicates whether the linked object updates the cached data for the linked object automatically or only when the container calls either the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">IOleObject::Update</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-update">IOleLink::Update</a> methods. The constants are used in the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a> interface.

## -enum-fields

### -field OLEUPDATE_ALWAYS:1

Update the link object whenever possible, this option corresponds to the <b>Automatic update</b> option in the <b>Links</b> dialog box.

### -field OLEUPDATE_ONCALL:3

Update the link object only when <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">IOleObject::Update</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-update">IOleLink::Update</a> is called, this option corresponds to the <b>Manual update</b> option in the <b>Links</b> dialog box.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getupdateoptions">IOleLink::GetUpdateOptions</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">IOleLink::SetUpdateOptions</a>
