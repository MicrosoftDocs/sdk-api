---
UID: NF:propidlbase.IEnumSTATPROPSETSTG.Skip
title: IEnumSTATPROPSETSTG::Skip (propidlbase.h)
description: Skips a specified number of STATPROPSETSTG structures in the enumeration sequence.helpviewer_keywords: ["IEnumSTATPROPSETSTG interface [Structured Storage]","Skip method","IEnumSTATPROPSETSTG.Skip","IEnumSTATPROPSETSTG::Skip","Skip","Skip method [Structured Storage]","Skip method [Structured Storage]","IEnumSTATPROPSETSTG interface","propidlbase/IEnumSTATPROPSETSTG::Skip","stg.ienumstatpropsetstg_skip"]
old-location: stg\ienumstatpropsetstg_skip.htm
tech.root: Stg
ms.assetid: 48275ca5-f9d1-42cb-b218-f51488a91bf8
ms.date: 12/05/2018
ms.keywords: IEnumSTATPROPSETSTG interface [Structured Storage],Skip method, IEnumSTATPROPSETSTG.Skip, IEnumSTATPROPSETSTG::Skip, Skip, Skip method [Structured Storage], Skip method [Structured Storage],IEnumSTATPROPSETSTG interface, propidlbase/IEnumSTATPROPSETSTG::Skip, stg.ienumstatpropsetstg_skip
f1_keywords:
- propidlbase/IEnumSTATPROPSETSTG.Skip
dev_langs:
- c++
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IEnumSTATPROPSETSTG.Skip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATPROPSETSTG::Skip


## -description


The <b>Skip</b> method skips a specified number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures in the enumeration sequence.


## -parameters




### -param celt

The number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures to skip.


## -returns



This method supports the following return values:




## -remarks



A positive value for the <i>celt</i> parameter skips forward in the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure enumeration. A negative value for the <i>celt</i> parameter skips backward in the <b>STATPROPSETSTG</b> structure enumeration.



