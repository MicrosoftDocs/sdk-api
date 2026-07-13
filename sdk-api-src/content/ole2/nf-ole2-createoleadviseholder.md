---
UID: NF:ole2.CreateOleAdviseHolder
title: CreateOleAdviseHolder function (ole2.h)
description: Creates an advise holder object for managing compound document notifications. It returns a pointer to the object's OLE implementation of the IOleAdviseHolder interface.
helpviewer_keywords: ["CreateOleAdviseHolder","CreateOleAdviseHolder function [COM]","_ole_CreateOleAdviseHolder","com.createoleadviseholder","ole2/CreateOleAdviseHolder"]
old-location: com\createoleadviseholder.htm
tech.root: com
ms.assetid: f76e074e-6814-4735-9417-d5970e73089f
ms.date: 12/05/2018
ms.keywords: CreateOleAdviseHolder, CreateOleAdviseHolder function [COM], _ole_CreateOleAdviseHolder, com.createoleadviseholder, ole2/CreateOleAdviseHolder
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateOleAdviseHolder
 - ole2/CreateOleAdviseHolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CreateOleAdviseHolder
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# CreateOleAdviseHolder function


## -description

Creates an advise holder object for managing compound document notifications. It returns a pointer to the object's OLE implementation of the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a> interface.

## -parameters

### -param ppOAHolder [out]

Address of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a> pointer variable that receives the interface pointer to the new advise holder object.

## -returns

This function returns S_OK on success and supports the standard return value E_OUTOFMEMORY.

## -remarks

The function <b>CreateOleAdviseHolder</b> creates an instance of an advise holder, which supports the OLE implementation of the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a> interface. The methods of this interface are intended to be used to implement the advisory methods of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>, and, when advisory connections have been set up with objects supporting an advisory sink, to send notifications of changes in the object to the advisory sink. The advise holder returned by <b>CreateOleAdviseHolder</b> will suffice for the great majority of applications. The OLE-provided implementation does not, however, support <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-enumadvise">IOleAdviseHolder::EnumAdvise</a>, so if you need to use this method, you will need to implement your own advise holder.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>
