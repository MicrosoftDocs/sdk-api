---
UID: NS:ocidl.tagCONNECTDATA
title: CONNECTDATA (ocidl.h)
description: Describes a connection that exists to a given connection point.
helpviewer_keywords: ["*LPCONNECTDATA","*PCONNECTDATA","CONNECTDATA","CONNECTDATA structure [COM]","LPCONNECTDATA","LPCONNECTDATA structure pointer [COM]","PCONNECTDATA","PCONNECTDATA structure pointer [COM]","_com_CONNECTDATA","com.connectdata","ocidl/CONNECTDATA","ocidl/LPCONNECTDATA","ocidl/PCONNECTDATA"]
old-location: com\connectdata.htm
tech.root: com
ms.assetid: 23312f89-2985-402d-aae4-cd7388137153
ms.date: 12/05/2018
ms.keywords: '*LPCONNECTDATA, *PCONNECTDATA, CONNECTDATA, CONNECTDATA structure [COM], LPCONNECTDATA, LPCONNECTDATA structure pointer [COM], PCONNECTDATA, PCONNECTDATA structure pointer [COM], _com_CONNECTDATA, com.connectdata, ocidl/CONNECTDATA, ocidl/LPCONNECTDATA, ocidl/PCONNECTDATA'
req.header: ocidl.h
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
req.typenames: CONNECTDATA, *PCONNECTDATA, *LPCONNECTDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCONNECTDATA
 - ocidl/tagCONNECTDATA
 - PCONNECTDATA
 - ocidl/PCONNECTDATA
 - CONNECTDATA
 - ocidl/CONNECTDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ocidl.h
api_name:
 - CONNECTDATA
---

# CONNECTDATA structure


## -description

Describes a connection that exists to a given connection point.

## -struct-fields

### -field pUnk

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on a connected advisory sink. The caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> using this pointer when the <b>CONNECTDATA</b> structure is no longer needed. The caller is responsible for calling <b>Release</b> for each <b>CONNECTDATA</b> structure enumerated through <a href="/windows/desktop/api/ocidl/nf-ocidl-ienumconnections-next">IEnumConnections::Next</a>.

### -field dwCookie

Connection value that is the same token that is returned originally from calls to <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">IConnectionPoint::Advise</a>. This token can be used to disconnect the sink pointed to by a <b>pUnk</b> by passing <b>dwCookie</b> to <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">IConnectionPoint::Unadvise</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
