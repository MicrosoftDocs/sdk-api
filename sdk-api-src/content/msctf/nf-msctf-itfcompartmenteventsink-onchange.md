---
UID: NF:msctf.ITfCompartmentEventSink.OnChange
title: ITfCompartmentEventSink::OnChange (msctf.h)
author: windows-sdk-content
description: ITfCompartmentEventSink::OnChange method
old-location: tsf\itfcompartmenteventsink_onchange.htm
tech.root: TSF
ms.assetid: 1756754c-6353-4296-bdb5-1cbef1d29ec5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfCompartmentEventSink interface [Text Services Framework],OnChange method, ITfCompartmentEventSink.OnChange, ITfCompartmentEventSink::OnChange, OnChange, OnChange method [Text Services Framework], OnChange method [Text Services Framework],ITfCompartmentEventSink interface, _tsf_itfcompartmenteventsink_onchange_ref, msctf/ITfCompartmentEventSink::OnChange, tsf.itfcompartmenteventsink_onchange
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfCompartmentEventSink.OnChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCompartmentEventSink::OnChange


## -description




## -parameters




### -param rguid [in]

Contains a GUID that identifies the compartment that changed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When this method is called, the data has changed. The new data can be obtained at this time by calling <a href="https://msdn.microsoft.com/31a9efbd-ebde-4877-a387-ebaccd97d732">ITfCompartment::GetValue</a>.


<a href="https://msdn.microsoft.com/1a1a175f-a24e-4f83-92d3-ac6a24f5f486">ITfCompartment::SetValue
        </a> will return E_UNEXPECTED if called from within this notification.




## -see-also




<a href="https://msdn.microsoft.com/31a9efbd-ebde-4877-a387-ebaccd97d732">ITfCompartment::GetValue
      </a>



<a href="https://msdn.microsoft.com/1a1a175f-a24e-4f83-92d3-ac6a24f5f486">ITfCompartment::SetValue
      </a>



<a href="https://msdn.microsoft.com/1bd464e7-9e34-4725-83f9-42e09ddf4778">ITfCompartmentEventSink</a>
 

 

