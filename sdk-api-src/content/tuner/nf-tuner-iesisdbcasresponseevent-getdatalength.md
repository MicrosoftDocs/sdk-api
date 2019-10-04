---
UID: NF:tuner.IESIsdbCasResponseEvent.GetDataLength
title: IESIsdbCasResponseEvent::GetDataLength (tuner.h)
author: windows-sdk-content
description: Gets the length of response data returned in anIsdbCasResponse event.
old-location: mstv\iesisdbcasresponseevent_getdatalength.htm
tech.root: mstv
ms.assetid: dc625c6f-84e8-4a82-b53c-717b33c10d04
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDataLength, GetDataLength method [DirectShow], GetDataLength method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetDataLength method, IESIsdbCasResponseEvent.GetDataLength, IESIsdbCasResponseEvent::GetDataLength, mstv.iesisdbcasresponseevent_getdatalength, tuner/IESIsdbCasResponseEvent::GetDataLength
ms.topic: method
f1_keywords: 
 - "tuner/IESIsdbCasResponseEvent.GetDataLength"
dev_langs:
 - c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESIsdbCasResponseEvent.GetDataLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESIsdbCasResponseEvent::GetDataLength


## -description


Gets the length of response data returned in an<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IsdbCasResponse</a> event.


## -parameters




### -param pRequestLength [out, retval]

Receives the length of the response data, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IESIsdbCasResponseEvent</a>
 

 

