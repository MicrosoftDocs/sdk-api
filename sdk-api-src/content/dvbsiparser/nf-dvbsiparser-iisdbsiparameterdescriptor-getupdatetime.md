---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetUpdateTime
title: IIsdbSIParameterDescriptor::GetUpdateTime (dvbsiparser.h)
description: Gets the time at which a parameter becomes valid from a service information (SI) parameter descriptor.
helpviewer_keywords: ["GetUpdateTime","GetUpdateTime method [Microsoft TV Technologies]","GetUpdateTime method [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","GetUpdateTime method","IIsdbSIParameterDescriptor.GetUpdateTime","IIsdbSIParameterDescriptor::GetUpdateTime","dvbsiparser/IIsdbSIParameterDescriptor::GetUpdateTime","mstv.iisdbsiparameterdescriptor_getupdatetime"]
old-location: mstv\iisdbsiparameterdescriptor_getupdatetime.htm
tech.root: mstv
ms.assetid: 9cfe8387-4edf-453b-b41b-768496eae76c
ms.date: 12/05/2018
ms.keywords: GetUpdateTime, GetUpdateTime method [Microsoft TV Technologies], GetUpdateTime method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetUpdateTime method, IIsdbSIParameterDescriptor.GetUpdateTime, IIsdbSIParameterDescriptor::GetUpdateTime, dvbsiparser/IIsdbSIParameterDescriptor::GetUpdateTime, mstv.iisdbsiparameterdescriptor_getupdatetime
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIsdbSIParameterDescriptor::GetUpdateTime
 - dvbsiparser/IIsdbSIParameterDescriptor::GetUpdateTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbSIParameterDescriptor.GetUpdateTime
---

# IIsdbSIParameterDescriptor::GetUpdateTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the time at which a parameter becomes valid from a service information (SI) parameter descriptor.

## -parameters

### -param pVal [out]

Receives the date/time value that indicates when the parameter becomes valid.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparameterdescriptor">IIsdbSIParameterDescriptor</a>