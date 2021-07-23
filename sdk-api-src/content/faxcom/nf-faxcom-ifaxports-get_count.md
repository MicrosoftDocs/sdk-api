---
UID: NF:faxcom.IFaxPorts.get_Count
title: IFaxPorts::get_Count (faxcom.h)
description: The IFaxPorts::get_Count method retrieves the number of fax ports attached to the connected fax server.
helpviewer_keywords: ["IFaxPorts interface [Fax Service]","get_Count method","IFaxPorts.get_Count","IFaxPorts::get_Count","_mfax_ifaxports_get_count","fax._mfax_ifaxports_get_count","faxcom/IFaxPorts::get_Count","get_Count","get_Count method [Fax Service]","get_Count method [Fax Service]","IFaxPorts interface"]
old-location: fax\_mfax_ifaxports_get_count.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7rp0.htm
ms.date: 12/05/2018
ms.keywords: IFaxPorts interface [Fax Service],get_Count method, IFaxPorts.get_Count, IFaxPorts::get_Count, _mfax_ifaxports_get_count, fax._mfax_ifaxports_get_count, faxcom/IFaxPorts::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxPorts interface
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxPorts::get_Count
 - faxcom/IFaxPorts::get_Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxPorts.get_Count
---

# IFaxPorts::get_Count


## -description

The <b>IFaxPorts::get_Count</b> method retrieves the number of fax ports attached to the connected fax server.

## -parameters

### -param pVal [out]

Type: <b>LONG*</b>

A pointer to a <b>LONG</b> that receives the number of fax ports attached to the connected fax server.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After calling the <b>IFaxPorts::get_Count</b> method, a fax client application can call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_item">IFaxPorts::get_Item</a> method to retrieve an interface pointer to one or more <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> objects.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">GetPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_item">IFaxPorts::get_Item</a>