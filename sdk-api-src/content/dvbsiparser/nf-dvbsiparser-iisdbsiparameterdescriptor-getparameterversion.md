---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetParameterVersion
title: IIsdbSIParameterDescriptor::GetParameterVersion (dvbsiparser.h)
description: Gets the version number of a parameter from a service information (SI) parameter descriptor. This version number is incremented by one each time the parameter is updated.
helpviewer_keywords: ["GetParameterVersion","GetParameterVersion method [Microsoft TV Technologies]","GetParameterVersion method [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","GetParameterVersion method","IIsdbSIParameterDescriptor.GetParameterVersion","IIsdbSIParameterDescriptor::GetParameterVersion","dvbsiparser/IIsdbSIParameterDescriptor::GetParameterVersion","mstv.iisdbsiparameterdescriptor_getparameterversion"]
old-location: mstv\iisdbsiparameterdescriptor_getparameterversion.htm
tech.root: mstv
ms.assetid: 8ca9d5d3-d96f-4437-9d22-0166a3fbc593
ms.date: 12/05/2018
ms.keywords: GetParameterVersion, GetParameterVersion method [Microsoft TV Technologies], GetParameterVersion method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetParameterVersion method, IIsdbSIParameterDescriptor.GetParameterVersion, IIsdbSIParameterDescriptor::GetParameterVersion, dvbsiparser/IIsdbSIParameterDescriptor::GetParameterVersion, mstv.iisdbsiparameterdescriptor_getparameterversion
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
 - IIsdbSIParameterDescriptor::GetParameterVersion
 - dvbsiparser/IIsdbSIParameterDescriptor::GetParameterVersion
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
 - IIsdbSIParameterDescriptor.GetParameterVersion
---

# IIsdbSIParameterDescriptor::GetParameterVersion


## -description

 Gets the version number of a parameter from a service information (SI) parameter descriptor. This version number is incremented by one each time the parameter is updated.

## -parameters

### -param pbVal [out]

Receives the version number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparameterdescriptor">IIsdbSIParameterDescriptor</a>