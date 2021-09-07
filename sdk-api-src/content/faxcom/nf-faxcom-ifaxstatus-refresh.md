---
UID: NF:faxcom.IFaxStatus.Refresh
title: IFaxStatus::Refresh (faxcom.h)
description: The Refresh method updates FaxStatus object information for the associated parent FaxPort object.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","Refresh method","IFaxStatus.Refresh","IFaxStatus::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_refresh","fax._mfax_ifaxstatus_mfax_ifaxstatus_refresh_cpp","fax._mfax_ifaxstatus_refresh","faxcom/IFaxStatus::Refresh"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_53c8.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],Refresh method, IFaxStatus.Refresh, IFaxStatus::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_refresh, fax._mfax_ifaxstatus_mfax_ifaxstatus_refresh_cpp, fax._mfax_ifaxstatus_refresh, faxcom/IFaxStatus::Refresh
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
 - IFaxStatus::Refresh
 - faxcom/IFaxStatus::Refresh
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
 - IFaxStatus.Refresh
 - IFaxStatus.Refresh
---

# IFaxStatus::Refresh


## -description

The <b>Refresh</b> method updates <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object information for the associated parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call the <b>IFaxStatus::Refresh</b> method to update the information for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. An application must call this method to poll a fax port for new status information. After you successfully call <b>IFaxStatus::Refresh</b>, you must call the appropriate <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a> interface method to retrieve new attribute values that are valid.

It is recommended that you limit calls to this method because frequent calls to <b>IFaxStatus::Refresh</b> can affect system performance.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>
