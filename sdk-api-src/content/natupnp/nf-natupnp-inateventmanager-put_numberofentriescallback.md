---
UID: NF:natupnp.INATEventManager.put_NumberOfEntriesCallback
title: INATEventManager::put_NumberOfEntriesCallback (natupnp.h)
description: The put_NumberOfEntriesCallback method enables the NAT application with UPnP technology to register a callback interface with the NAT. The system calls the first method in this callback interface if the number of NAT port mappings changes.
helpviewer_keywords: ["INATEventManager interface [ICS/ICF]","put_NumberOfEntriesCallback method","INATEventManager.put_NumberOfEntriesCallback","INATEventManager::put_NumberOfEntriesCallback","_ics_inateventmanager_put_numberofentriescallback","ics.inateventmanager_put_numberofentriescallback","natupnp/INATEventManager::put_NumberOfEntriesCallback","put_NumberOfEntriesCallback","put_NumberOfEntriesCallback method [ICS/ICF]","put_NumberOfEntriesCallback method [ICS/ICF]","INATEventManager interface"]
old-location: ics\inateventmanager_put_numberofentriescallback.htm
tech.root: ics
ms.assetid: a02a0f1e-5085-444b-adc4-c3cd919f7e25
ms.date: 12/05/2018
ms.keywords: INATEventManager interface [ICS/ICF],put_NumberOfEntriesCallback method, INATEventManager.put_NumberOfEntriesCallback, INATEventManager::put_NumberOfEntriesCallback, _ics_inateventmanager_put_numberofentriescallback, ics.inateventmanager_put_numberofentriescallback, natupnp/INATEventManager::put_NumberOfEntriesCallback, put_NumberOfEntriesCallback, put_NumberOfEntriesCallback method [ICS/ICF], put_NumberOfEntriesCallback method [ICS/ICF],INATEventManager interface
req.header: natupnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Hnetcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INATEventManager::put_NumberOfEntriesCallback
 - natupnp/INATEventManager::put_NumberOfEntriesCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INATEventManager.put_NumberOfEntriesCallback
---

# INATEventManager::put_NumberOfEntriesCallback


## -description

The <b>put_NumberOfEntriesCallback</b> method enables the NAT application with UPnP technology to register a callback interface with the NAT. The system calls the first method in this callback interface if the number of NAT port mappings changes.

## -parameters

### -param pUnk [in]

Pointer to an object that supports either the 
<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface or the 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. See the Remarks section for more information.

## -returns

If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>

## -remarks

The object referred to by <i>pUnk</i> must either support the 
<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inatnumberofentriescallback">INATNumberOfEntriesCallback</a> interface or the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. The NAT first queries <i>pUnk</i> for the 
<b>INATNumberOfEntriesCallback</b> interface. If this interface is not supported, the NAT queries <i>pUnk</i> for the <b>IDispatch</b> interface. If the <b>IDispatch</b> interface is not supported, the <b>NumberOfEntriesCallback</b> method returns E_FAIL.

If only <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> is supported, the NAT invokes the callback by calling <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a> with the dispatch ID specified as zero, which indicates the default method. This <b>IDispatch</b> method is passed the same parameters as the 
<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inatnumberofentriescallback">INATNumberOfEntriesCallback</a> method, except that the first parameter passed is a string that indicates the reason the callback is invoked.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inateventmanager">INATEventManager</a>



<a href="/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inatnumberofentriescallback">INATNumberOfEntriesCallback</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>