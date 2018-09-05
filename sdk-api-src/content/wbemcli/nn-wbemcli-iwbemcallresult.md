---
UID: NN:wbemcli.IWbemCallResult
title: IWbemCallResult
author: windows-sdk-content
description: Used for semisynchronous calls of the IWbemServices interface. When making such calls, the called IWbemServices method returns immediately, along with an IWbemCallResult object.
old-location: wmi\iwbemcallresult.htm
old-project: WmiSdk
ms.assetid: f0aa0233-3b9b-4757-bfdc-26d9fd556ce9
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemCallResult, IWbemCallResult interface [Windows Management Instrumentation], IWbemCallResult interface [Windows Management Instrumentation],described, _hmm_iwbemcallresult, wbemcli/IWbemCallResult, wmi.iwbemcallresult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemcli.h
api_name:
 - IWbemCallResult
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemCallResult interface


## -description


The 
<b>IWbemCallResult</b> interface is used for semisynchronous calls of the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface. When making such calls, the called 
<b>IWbemServices</b> method returns immediately, along with an 
<b>IWbemCallResult</b> object. Periodically, you can poll the returned 
<b>IWbemCallResult</b> object to determine the status of the call. You can obtain the result of the original 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> call after it is complete by calling 
<a href="https://msdn.microsoft.com/5a600fd8-87d8-446d-93da-5b22fd575a11">IWbemCallResult::GetCallStatus</a>.

This call-return paradigm is useful in cases where a thread cannot afford to be blocked for more than a few seconds because it is servicing other tasks, such as processing window messages.

Not all 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> methods support this interface because it is not required for all of them. The intent is to allow nonblocking, synchronous operation (semisynchronous operation) for all relevant operations. Because many of the 
<b>IWbemServices</b> methods are already nonblocking due to the use of enumerators or other constructs, only 
the following methods need this helper interface to support semisynchronous operation:
<ul>
<li>
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">OpenNamespace</a>
</li>
<li>
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">GetObject</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">PutInstance</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">PutClass</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1266d93a-776c-481d-b343-826a5c808d24">DeleteClass</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">DeleteInstance</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">ExecMethod</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemCallResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemCallResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemCallResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a600fd8-87d8-446d-93da-5b22fd575a11">GetCallStatus</a>
</td>
<td align="left" width="63%">
Reports whether a semisynchronous call was successful.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06603f26-587f-4aff-8ae3-7f77f9b266f5">GetResultObject</a>
</td>
<td align="left" width="63%">
Returns an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object, which is the result of a semisynchronous call to 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64a4fc4c-f479-4b03-847c-041508e55532">GetResultServices</a>
</td>
<td align="left" width="63%">
Returns the result of a semisynchronous call to 
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">IWbemServices::OpenNamespace</a> verb action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a022519-c112-42d4-b777-c3828439f7dd">GetResultString</a>
</td>
<td align="left" width="63%">
Returns an object path, which is the result of a semisynchronous call to 
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>.

</td>
</tr>
</table> 

