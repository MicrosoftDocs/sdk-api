---
UID: NN:docobj.IPrint
title: IPrint (docobj.h)
description: Enables compound documents in general and active documents in particular to support programmatic printing.
helpviewer_keywords: ["IPrint","IPrint interface [COM]","IPrint interface [COM]","described","_ctrl_iprint","com.iprint","docobj/IPrint"]
old-location: com\iprint.htm
tech.root: com
ms.assetid: eb0d15c0-8a34-4211-b840-29d5862cf767
ms.date: 12/05/2018
ms.keywords: IPrint, IPrint interface [COM], IPrint interface [COM],described, _ctrl_iprint, com.iprint, docobj/IPrint
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
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
 - IPrint
 - docobj/IPrint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IPrint
---

# IPrint interface


## -description

Enables compound documents in general and active documents in particular to support programmatic printing.

## -inheritance

The <b>IPrint</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrint</b> also has these types of members:

## -remarks

After a document is loaded, containers and other clients can call <a href="/windows/desktop/api/docobj/nf-docobj-iprint-print">IPrint::Print</a> to instruct a document to print itself, specifying printing control flags, the target device, the particular pages to print, and other options. The client can control the continuation of printing by calling the <a href="/windows/desktop/api/docobj/nn-docobj-icontinuecallback">IContinueCallback</a> interface. 


An object that implements <b>IPrint</b> registers itself with the <b>Printable</b> key stored under its CLSID as follows:


<b>HKEY_CLASSES_ROOT\CLSID\{...}\Printable</b>



Callers determine whether a particular object class supports programmatic printing of its persistent state by looking in the registry for this key.
