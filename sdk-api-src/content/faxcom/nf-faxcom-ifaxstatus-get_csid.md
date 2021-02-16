---
UID: NF:faxcom.IFaxStatus.get_Csid
title: IFaxStatus::get_Csid (faxcom.h)
description: Retrieves the Csid property for the FaxStatus object of a parent FaxPort object. The Csid property is a string that contains called station identifier (CSID) information, typically the fax number of the receiving device.
helpviewer_keywords: ["Csid property [Fax Service]","Csid property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","Csid property","IFaxStatus.Csid","IFaxStatus.get_Csid","IFaxStatus::Csid","IFaxStatus::get_Csid","_mfax_ifaxstatus_get_csid","fax._mfax_ifaxstatus_get_csid","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_csid_cpp","faxcom/IFaxStatus::Csid","faxcom/IFaxStatus::get_Csid","get_Csid"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_csid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6k2s.htm
ms.date: 12/05/2018
ms.keywords: Csid property [Fax Service], Csid property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],Csid property, IFaxStatus.Csid, IFaxStatus.get_Csid, IFaxStatus::Csid, IFaxStatus::get_Csid, _mfax_ifaxstatus_get_csid, fax._mfax_ifaxstatus_get_csid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_csid_cpp, faxcom/IFaxStatus::Csid, faxcom/IFaxStatus::get_Csid, get_Csid
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
 - IFaxStatus::get_Csid
 - faxcom/IFaxStatus::get_Csid
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
 - IFaxStatus.Csid
 - IFaxStatus.get_Csid
---

# IFaxStatus::get_Csid


## -description

Retrieves the <b>Csid</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Csid</b> property is a string that contains called station identifier (CSID) information, typically the fax number of the receiving device.

This property is read-only.

## -parameters

## -remarks

If the CSID information is not available, the <b>IFaxStatus::get_Csid</b> method returns an empty string.

The <b>IFaxStatus::get_Csid</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>