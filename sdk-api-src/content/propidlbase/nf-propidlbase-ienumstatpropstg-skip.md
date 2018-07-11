---
UID: NF:propidlbase.IEnumSTATPROPSTG.Skip
title: IEnumSTATPROPSTG::Skip
author: windows-sdk-content
description: Skips the specified number of STATPROPSTG structures in the enumeration sequence.
old-location: stg\ienumstatpropstg_skip.htm
old-project: stg
ms.assetid: e70e4668-d52c-4135-948b-c8f5d141e6a2
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IEnumSTATPROPSTG interface [Structured Storage],Skip method, IEnumSTATPROPSTG.Skip, IEnumSTATPROPSTG::Skip, Skip, Skip method [Structured Storage], Skip method [Structured Storage],IEnumSTATPROPSTG interface, propidlbase/IEnumSTATPROPSTG::Skip, stg.ienumstatpropstg_skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STATPROPSTG
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
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IEnumSTATPROPSTG::Skip


## -description


The <b>Skip</b> method skips the specified number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures in the enumeration sequence.


## -parameters




### -param celt

The number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures to skip.


## -returns



This method supports the following return values:




## -remarks



A positive value for the <i>celt</i> parameter skips forward in the <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structure enumeration. A negative value for the <i>celt</i> parameter skips backward in the <b>STATPROPSTG</b> structure enumeration.



