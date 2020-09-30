---
UID: NF:faxcom.IFaxStatus.get_Tsid
title: IFaxStatus::get_Tsid (faxcom.h)
description: Retrieves the Tsid property for the FaxStatus object of a parent FaxPort object. The Tsid property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","Tsid property","IFaxStatus.Tsid","IFaxStatus.get_Tsid","IFaxStatus::Tsid","IFaxStatus::get_Tsid","Tsid property [Fax Service]","Tsid property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_tsid","fax._mfax_ifaxstatus_get_tsid","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_tsid_cpp","faxcom/IFaxStatus::Tsid","faxcom/IFaxStatus::get_Tsid","get_Tsid"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_22p0.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],Tsid property, IFaxStatus.Tsid, IFaxStatus.get_Tsid, IFaxStatus::Tsid, IFaxStatus::get_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_tsid_cpp, faxcom/IFaxStatus::Tsid, faxcom/IFaxStatus::get_Tsid, get_Tsid
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
 - IFaxStatus::get_Tsid
 - faxcom/IFaxStatus::get_Tsid
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
 - IFaxStatus.Tsid
 - IFaxStatus.get_Tsid
---

# IFaxStatus::get_Tsid


## -description

Retrieves the <b>Tsid</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Tsid</b> property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.

This property is read-only.

## -parameters

## -remarks

The <b>Tsid</b> property is set for both inbound and outbound fax transmissions. If the TSID information is not available, the <b>IFaxStatus::get_Tsid</b> method returns an empty string.

The <b>IFaxStatus::get_Tsid</b> method allocates the memory required for the buffer pointed to by the pVal parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>