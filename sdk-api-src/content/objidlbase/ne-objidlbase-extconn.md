---
UID: NE:objidlbase.tagEXTCONN
title: EXTCONN (objidlbase.h)
description: The EXTCONN (objidlbase.h) enumeration specifies the type of external connection existing on an embedded object.
helpviewer_keywords: ["EXTCONN","EXTCONN enumeration [COM]","EXTCONN_CALLABLE","EXTCONN_STRONG","EXTCONN_WEAK","_com_EXTCONN","com.extconn","objidlbase/EXTCONN","objidlbase/EXTCONN_CALLABLE","objidlbase/EXTCONN_STRONG","objidlbase/EXTCONN_WEAK"]
old-location: com\extconn.htm
tech.root: com
ms.assetid: 95c7de47-9f81-4316-99b8-0f5f0aa54d65
ms.date: 08/13/2022
ms.keywords: EXTCONN, EXTCONN enumeration [COM], EXTCONN_CALLABLE, EXTCONN_STRONG, EXTCONN_WEAK, _com_EXTCONN, com.extconn, objidlbase/EXTCONN, objidlbase/EXTCONN_CALLABLE, objidlbase/EXTCONN_STRONG, objidlbase/EXTCONN_WEAK
req.header: objidlbase.h
req.include-header: Objidl.h
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
req.typenames: EXTCONN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEXTCONN
 - objidlbase/tagEXTCONN
 - EXTCONN
 - objidlbase/EXTCONN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - EXTCONN
---

# EXTCONN enumeration


## -description

Specifies the type of external connection existing on an embedded object.

## -enum-fields

### -field EXTCONN_STRONG:0x1

The external connection is a link. If this value is specified, the external connection must keep the object alive until all strong external connections are cleared through <a href="/windows/desktop/api/objidl/nf-objidl-iexternalconnection-releaseconnection">IExternalConnection::ReleaseConnection</a>.

### -field EXTCONN_WEAK:0x2

This value is not used.

### -field EXTCONN_CALLABLE:0x4

This value is not used.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iexternalconnection-addconnection">IExternalConnection::AddConnection</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iexternalconnection-releaseconnection">IExternalConnection::ReleaseConnection</a>
