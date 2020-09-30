---
UID: NF:imapi.IDiscRecorder.SetRecorderProperties
title: IDiscRecorder::SetRecorderProperties (imapi.h)
description: Accepts an IPropertyStorage pointer for an object with all the properties that the application wishes to change. Sparse settings are supported.
helpviewer_keywords: ["IDiscRecorder interface [IMAPI]","SetRecorderProperties method","IDiscRecorder.SetRecorderProperties","IDiscRecorder::SetRecorderProperties","SetRecorderProperties","SetRecorderProperties method [IMAPI]","SetRecorderProperties method [IMAPI]","IDiscRecorder interface","_win32_idiscrecorder_setrecorderproperties","base.idiscrecorder_setrecorderproperties","imapi.idiscrecorder_setrecorderproperties","imapi/IDiscRecorder::SetRecorderProperties"]
old-location: imapi\idiscrecorder_setrecorderproperties.htm
tech.root: imapi
ms.assetid: 8da0add7-6a9d-46f4-b34c-7ea9aa0b7d3a
ms.date: 12/05/2018
ms.keywords: IDiscRecorder interface [IMAPI],SetRecorderProperties method, IDiscRecorder.SetRecorderProperties, IDiscRecorder::SetRecorderProperties, SetRecorderProperties, SetRecorderProperties method [IMAPI], SetRecorderProperties method [IMAPI],IDiscRecorder interface, _win32_idiscrecorder_setrecorderproperties, base.idiscrecorder_setrecorderproperties, imapi.idiscrecorder_setrecorderproperties, imapi/IDiscRecorder::SetRecorderProperties
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
 - IDiscRecorder::SetRecorderProperties
 - imapi/IDiscRecorder::SetRecorderProperties
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
 - IDiscRecorder.SetRecorderProperties
---

# IDiscRecorder::SetRecorderProperties


## -description

Accepts an 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> pointer for an object with all the properties that the application wishes to change. Sparse settings are supported. It is recommended, however, to query for a property set using 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getrecorderproperties">GetRecorderProperties</a>, modify only those settings of interest, and then call 
<b>SetRecorderProperties</b> to change all values simultaneously.

## -parameters

### -param pPropStg [in]

Pointer to the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface that the disc recorder can use to retrieve new settings on various properties.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

Some properties are read-only, such as MaxWriteSpeed. Both read-only properties and unsupported properties are ignored without generating an error (see IMAPI_S_PROPERTIESIGNORED). For example, someone could submit a property set to this interface and attempt to change the MaxWriteSpeed and ClearlyNeverHeardOfBefore properties. Since MaxWriteSpeed is read-only and ClearlyNeverHeardOfBefore is an unknown value, both properties are ignored and the method succeeds.

After calling 
<b>SetRecorderProperties</b>, an application should verify property settings by calling 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getrecorderproperties">GetRecorderProperties</a>.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>