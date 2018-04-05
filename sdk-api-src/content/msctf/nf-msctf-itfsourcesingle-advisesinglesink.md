---
UID: NF:msctf.ITfSourceSingle.AdviseSingleSink
title: ITfSourceSingle::AdviseSingleSink method
author: windows-driver-content
description: ITfSourceSingle::AdviseSingleSink method
old-location: tsf\itfsourcesingle_advisesinglesink.htm
old-project: TSF
ms.assetid: d9231f36-24c4-4d46-97e7-518f5fcc1ce2
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: AdviseSingleSink method [Text Services Framework], AdviseSingleSink method [Text Services Framework], ITfSourceSingle interface, AdviseSingleSink,ITfSourceSingle.AdviseSingleSink, IID_ITfCleanupContextDurationSink, IID_ITfFunctionProvider, ITfSourceSingle, ITfSourceSingle interface [Text Services Framework], AdviseSingleSink method, ITfSourceSingle::AdviseSingleSink, _tsf_itfsourcesingle_advisesinglesink_ref, msctf/ITfSourceSingle::AdviseSingleSink, tsf.itfsourcesingle_advisesinglesink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfSourceSingle.AdviseSingleSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfSourceSingle::AdviseSingleSink method


## -description




## -parameters




### -param tid [in]

Contains a <b>TfClientId</b> value that identifies the client.


### -param riid [in]

Identifies the type of advise sink to install.

This parameter can be one of the following values when the <a href="https://msdn.microsoft.com/01e60ede-b871-4b38-b2ee-24f79c5b3e80">ITfSourceSingle</a> object is obtained from an <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a> object.

This parameter can be one of the following values when the <b>ITfSourceSingle</b> object is obtained from an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> object.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IID_ITfCleanupContextDurationSink"></a><a id="iid_itfcleanupcontextdurationsink"></a><a id="IID_ITFCLEANUPCONTEXTDURATIONSINK"></a><dl>
<dt><b>IID_ITfCleanupContextDurationSink</b></dt>
</dl>
</td>
<td width="60%">
Installs a <a href="https://msdn.microsoft.com/2bbdc26a-5543-4de4-b347-2062be593c4b">ITfCleanupContextDurationSink</a> advise sink.

</td>
</tr>
<tr>
<td width="40%"><a id="IID_ITfFunctionProvider"></a><a id="iid_itffunctionprovider"></a><a id="IID_ITFFUNCTIONPROVIDER"></a><dl>
<dt><b>IID_ITfFunctionProvider</b></dt>
</dl>
</td>
<td width="60%">
Registers the client as a function provider. The <i>punk</i> parameter is an <a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">ITfFunctionProvider</a> interface pointer.

</td>
</tr>
</table>
 


### -param punk [in]

Pointer to the advise sink <b>IUnknown</b> pointer.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_CANNOTCONNECT</b></dt>
</dl>
</td>
<td width="60%">
The advise sink cannot be installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_ADVISELIMIT</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of advise sinks has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f88ebef7-2796-4076-892f-28fac6e143de">ITfCleanupContextSink
      </a>



<a href="https://msdn.microsoft.com/e63fd561-1157-49b1-a981-e578d9538876">
        ITfFunctionProvider
      </a>



<a href="https://msdn.microsoft.com/01e60ede-b871-4b38-b2ee-24f79c5b3e80">ITfSourceSingle</a>
 

 

