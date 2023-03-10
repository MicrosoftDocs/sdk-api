---
UID: NF:oleidl.IOleLink.GetUpdateOptions
title: IOleLink::GetUpdateOptions (oleidl.h)
description: Retrieves a value indicating how often the linked object updates its cached data.
helpviewer_keywords: ["GetUpdateOptions","GetUpdateOptions method [COM]","GetUpdateOptions method [COM]","IOleLink interface","IOleLink interface [COM]","GetUpdateOptions method","IOleLink.GetUpdateOptions","IOleLink::GetUpdateOptions","_ole_iolelink_getupdateoptions","com.iolelink_getupdateoptions","oleidl/IOleLink::GetUpdateOptions"]
old-location: com\iolelink_getupdateoptions.htm
tech.root: com
ms.assetid: 2cb91b48-0026-4afa-80ab-16ac6fbce04d
ms.date: 12/05/2018
ms.keywords: GetUpdateOptions, GetUpdateOptions method [COM], GetUpdateOptions method [COM],IOleLink interface, IOleLink interface [COM],GetUpdateOptions method, IOleLink.GetUpdateOptions, IOleLink::GetUpdateOptions, _ole_iolelink_getupdateoptions, com.iolelink_getupdateoptions, oleidl/IOleLink::GetUpdateOptions
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleLink::GetUpdateOptions
 - oleidl/IOleLink::GetUpdateOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink.GetUpdateOptions
---

# IOleLink::GetUpdateOptions


## -description

Retrieves a value indicating how often the linked object updates its cached data.

## -parameters

### -param pdwUpdateOpt [out]

A pointer to a variable that receives the current value for the linked object's update option, indicating how often the linked object updates the cached data for the linked object. The possible values for <i>pdwUpdateOpt</i> are taken from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-oleupdate">OLEUPDATE</a>.

## -returns

This method returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">IOleLink::SetUpdateOptions</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>