---
UID: NF:vidcap.IKsNodeControl.put_KsControl
title: IKsNodeControl::put_KsControl (vidcap.h)
description: Provides an instance of the IKsControl interface to the extension unit.
helpviewer_keywords: ["IKsNodeControl interface [DirectShow]","put_KsControl method","IKsNodeControl.put_KsControl","IKsNodeControl::put_KsControl","IKsNodeControlput_KsControl","dshow.iksnodecontrol_put_kscontrol","put_KsControl","put_KsControl method [DirectShow]","put_KsControl method [DirectShow]","IKsNodeControl interface","vidcap/IKsNodeControl::put_KsControl"]
old-location: dshow\iksnodecontrol_put_kscontrol.htm
tech.root: dshow
ms.assetid: 145967fc-3124-4e3b-b1ce-a381ea97cb89
ms.date: 12/05/2018
ms.keywords: IKsNodeControl interface [DirectShow],put_KsControl method, IKsNodeControl.put_KsControl, IKsNodeControl::put_KsControl, IKsNodeControlput_KsControl, dshow.iksnodecontrol_put_kscontrol, put_KsControl, put_KsControl method [DirectShow], put_KsControl method [DirectShow],IKsNodeControl interface, vidcap/IKsNodeControl::put_KsControl
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IKsNodeControl::put_KsControl
 - vidcap/IKsNodeControl::put_KsControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsNodeControl.put_KsControl
---

# IKsNodeControl::put_KsControl


## -description

Provides an instance of the <b>IKsControl</b> interface to the extension unit.

## -parameters

### -param pKsControl [in]

Pointer to the <b>IKsControl</b> interface, typed as a void pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The KsProxy filter calls this method with a pointer to its own <b>IKsControl</b> interface. The extension unit should cache the pointer.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-iksnodecontrol">IKsNodeControl Interface</a>