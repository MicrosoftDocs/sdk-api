---
UID: NF:objidl.IEnumSTATSTG.Skip
title: IEnumSTATSTG::Skip (objidl.h)
description: Skips a specified number of STATSTG structures in the enumeration sequence.
helpviewer_keywords: ["IEnumSTATSTG interface [Structured Storage]","Skip method","IEnumSTATSTG.Skip","IEnumSTATSTG::Skip","Skip","Skip method [Structured Storage]","Skip method [Structured Storage]","IEnumSTATSTG interface","objidl/IEnumSTATSTG::Skip","stg.ienumstatstg_skip"]
old-location: stg\ienumstatstg_skip.htm
tech.root: Stg
ms.assetid: 97d785d9-961c-44af-a0a0-1d2f610e6c9a
ms.date: 12/05/2018
ms.keywords: IEnumSTATSTG interface [Structured Storage],Skip method, IEnumSTATSTG.Skip, IEnumSTATSTG::Skip, Skip, Skip method [Structured Storage], Skip method [Structured Storage],IEnumSTATSTG interface, objidl/IEnumSTATSTG::Skip, stg.ienumstatstg_skip
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumSTATSTG::Skip
 - objidl/IEnumSTATSTG::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATSTG.Skip
---

# IEnumSTATSTG::Skip


## -description

The <b>Skip</b> method skips a specified number 
   of <a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structures in the enumeration 
   sequence.

## -parameters

### -param celt

The number of <a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structures to skip.

## -returns

This method supports the following return values:

| Return code | Description |
|----------------|---------------|
| S_OK | The specified number of **STATSTG** structures that were successfully skipped. |
| S_FALSE | The number of **STATSTG** structures skipped is less than the *celt* parameter. |
