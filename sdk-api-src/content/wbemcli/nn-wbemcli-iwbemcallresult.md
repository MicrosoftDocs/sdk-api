---
UID: NN:wbemcli.IWbemCallResult
title: IWbemCallResult (wbemcli.h)
description: Used for semisynchronous calls of the IWbemServices interface. When making such calls, the called IWbemServices method returns immediately, along with an IWbemCallResult object.
helpviewer_keywords: ["IWbemCallResult","IWbemCallResult interface [Windows Management Instrumentation]","IWbemCallResult interface [Windows Management Instrumentation]","described","_hmm_iwbemcallresult","wbemcli/IWbemCallResult","wmi.iwbemcallresult"]
old-location: wmi\iwbemcallresult.htm
tech.root: wmi
ms.assetid: f0aa0233-3b9b-4757-bfdc-26d9fd556ce9
ms.date: 12/05/2018
ms.keywords: IWbemCallResult, IWbemCallResult interface [Windows Management Instrumentation], IWbemCallResult interface [Windows Management Instrumentation],described, _hmm_iwbemcallresult, wbemcli/IWbemCallResult, wmi.iwbemcallresult
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IWbemCallResult
 - wbemcli/IWbemCallResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemcli.h
api_name:
 - IWbemCallResult
---

# IWbemCallResult interface


## -description

The 
<b>IWbemCallResult</b> interface is used for semisynchronous calls of the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface. When making such calls, the called 
<b>IWbemServices</b> method returns immediately, along with an 
<b>IWbemCallResult</b> object. Periodically, you can poll the returned 
<b>IWbemCallResult</b> object to determine the status of the call. You can obtain the result of the original 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> call after it is complete by calling 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus">IWbemCallResult::GetCallStatus</a>.

This call-return paradigm is useful in cases where a thread cannot afford to be blocked for more than a few seconds because it is servicing other tasks, such as processing window messages.

Not all 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> methods support this interface because it is not required for all of them. The intent is to allow nonblocking, synchronous operation (semisynchronous operation) for all relevant operations. Because many of the 
<b>IWbemServices</b> methods are already nonblocking due to the use of enumerators or other constructs, only 
the following methods need this helper interface to support semisynchronous operation:
<ul>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">OpenNamespace</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">GetObject</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">PutInstance</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">PutClass</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">DeleteClass</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">DeleteInstance</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">ExecMethod</a>
</li>
</ul>

## -inheritance

The <b>IWbemCallResult</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemCallResult</b> also has these types of members:

