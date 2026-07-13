---
UID: NN:wsmandisp.IWSManEnumerator
title: IWSManEnumerator (wsmandisp.h)
description: Represents a stream of results returned from operations such as a WS-Management protocol WS-Enumeration:Enumerate operation.
helpviewer_keywords: ["IWSManEnumerator","IWSManEnumerator interface [Windows Remote Management]","IWSManEnumerator interface [Windows Remote Management]","described","winrm.iwsmanenumerator","wsmandisp/IWSManEnumerator"]
old-location: winrm\iwsmanenumerator.htm
tech.root: winrm
ms.assetid: c7afac5d-946f-49ec-a7d0-de558ed2144b
ms.date: 12/05/2018
ms.keywords: IWSManEnumerator, IWSManEnumerator interface [Windows Remote Management], IWSManEnumerator interface [Windows Remote Management],described, winrm.iwsmanenumerator, wsmandisp/IWSManEnumerator
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManEnumerator
 - wsmandisp/IWSManEnumerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEnumerator
---

# IWSManEnumerator interface


## -description

Represents a stream of results returned from  operations such as a WS-Management protocol <a href="/windows/desktop/WinRM/windows-remote-management-glossary">WS-Enumeration</a>:Enumerate operation.

## -inheritance

The <b>IWSManEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSManEnumerator</b> also has these types of members:

## -remarks

The corresponding scripting object is <a href="/windows/desktop/WinRM/enumerator">Enumerator</a>.

To limit the number of items that are read, set the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get_batchitems">IWSManSession::BatchItems</a> property.

Be aware that freeing the enumeration object clears pending enumeration requests.

## -see-also

<a href="/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
