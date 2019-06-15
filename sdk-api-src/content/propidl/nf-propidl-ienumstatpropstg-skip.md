---
UID: NF:propidl.IEnumSTATPROPSTG.Skip
title: IEnumSTATPROPSTG::Skip (propidl.h)
author: windows-sdk-content
description: Skips the specified number of STATPROPSTG structures in the enumeration sequence.
old-location: stg\ienumstatpropstg_skip.htm
tech.root: Stg
ms.assetid: e70e4668-d52c-4135-948b-c8f5d141e6a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSTATPROPSTG interface [Structured Storage],Skip method, IEnumSTATPROPSTG.Skip, IEnumSTATPROPSTG::Skip, Skip, Skip method [Structured Storage], Skip method [Structured Storage],IEnumSTATPROPSTG interface, propidlbase/IEnumSTATPROPSTG::Skip, stg.ienumstatpropstg_skip
ms.topic: method
f1_keywords: ["propidl/IEnumSTATPROPSTG.Skip"]
req.header: propidl.h
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
 - IEnumSTATPROPSTG.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATPROPSTG::Skip


## -description


The <b>Skip</b> method skips the specified number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagstatpropstg">STATPROPSTG</a> structures in the enumeration sequence.


## -parameters




### -param celt

The number of <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagstatpropstg">STATPROPSTG</a> structures to skip.


## -returns



This method supports the following return values:




## -remarks



A positive value for the <i>celt</i> parameter skips forward in the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagstatpropstg">STATPROPSTG</a> structure enumeration. A negative value for the <i>celt</i> parameter skips backward in the <b>STATPROPSTG</b> structure enumeration.



