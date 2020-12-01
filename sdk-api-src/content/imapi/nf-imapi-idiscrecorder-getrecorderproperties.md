---
UID: NF:imapi.IDiscRecorder.GetRecorderProperties
title: IDiscRecorder::GetRecorderProperties (imapi.h)
description: Retrieves a pointer to an IPropertyStorage interface.
helpviewer_keywords: ["GetRecorderProperties","GetRecorderProperties method [IMAPI]","GetRecorderProperties method [IMAPI]","IDiscRecorder interface","IDiscRecorder interface [IMAPI]","GetRecorderProperties method","IDiscRecorder.GetRecorderProperties","IDiscRecorder::GetRecorderProperties","_win32_idiscrecorder_getrecorderproperties","base.idiscrecorder_getrecorderproperties","imapi.idiscrecorder_getrecorderproperties","imapi/IDiscRecorder::GetRecorderProperties"]
old-location: imapi\idiscrecorder_getrecorderproperties.htm
tech.root: imapi
ms.assetid: 24d46cbc-56fd-4c9f-933c-0207dea5ada5
ms.date: 12/05/2018
ms.keywords: GetRecorderProperties, GetRecorderProperties method [IMAPI], GetRecorderProperties method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetRecorderProperties method, IDiscRecorder.GetRecorderProperties, IDiscRecorder::GetRecorderProperties, _win32_idiscrecorder_getrecorderproperties, base.idiscrecorder_getrecorderproperties, imapi.idiscrecorder_getrecorderproperties, imapi/IDiscRecorder::GetRecorderProperties
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscRecorder::GetRecorderProperties
 - imapi/IDiscRecorder::GetRecorderProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder.GetRecorderProperties
---

# IDiscRecorder::GetRecorderProperties


## -description

Retrieves a pointer to an 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface.

## -parameters

### -param ppPropStg [out]

Pointer to an 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface to the property set with all current properties defined.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

Properties are not retained after IMAPI is closed. A property set format is convenient for IMAPI because it stores an ID/TYPE/VALUE combination, as well as ID/NAME associations. Each combination is a single property, and IMAPI uses these properties for various values that are unique to specific recorders. For example, most recorders would support a WriteSpeed property.

The caller can then modify properties by calling 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-setrecorderproperties">SetRecorderProperties</a>. Current properties include the following:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>