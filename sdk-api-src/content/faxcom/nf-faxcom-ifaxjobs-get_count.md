---
UID: NF:faxcom.IFaxJobs.get_Count
title: IFaxJobs::get_Count (faxcom.h)
description: The IFaxJobs::get_Count method returns the number of queued fax jobs associated with the connected fax server.
helpviewer_keywords: ["IFaxJobs interface [Fax Service]","get_Count method","IFaxJobs.get_Count","IFaxJobs::get_Count","_mfax_ifaxjobs_get_count","fax._mfax_ifaxjobs_get_count","faxcom/IFaxJobs::get_Count","get_Count","get_Count method [Fax Service]","get_Count method [Fax Service]","IFaxJobs interface"]
old-location: fax\_mfax_ifaxjobs_get_count.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_33zo.htm
ms.date: 12/05/2018
ms.keywords: IFaxJobs interface [Fax Service],get_Count method, IFaxJobs.get_Count, IFaxJobs::get_Count, _mfax_ifaxjobs_get_count, fax._mfax_ifaxjobs_get_count, faxcom/IFaxJobs::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxJobs interface
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
 - IFaxJobs::get_Count
 - faxcom/IFaxJobs::get_Count
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
 - IFaxJobs.get_Count
---

# IFaxJobs::get_Count


## -description

The <b>IFaxJobs::get_Count</b> method returns the number of queued fax jobs associated with the connected fax server.

## -parameters

### -param pVal [out]

Type: <b>LONG*</b>

A pointer to a <b>LONG</b> that receives the number of fax jobs associated with the connected fax server.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After calling the <b>IFaxJobs::get_Count</b> method, a fax client application can call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxjobs-get_item">IFaxJobs::get_Item</a> method to retrieve interface pointers to one or more <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> objects.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getjobs-vb">GetJobs</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxjobs-get_item">IFaxJobs::get_Item</a>