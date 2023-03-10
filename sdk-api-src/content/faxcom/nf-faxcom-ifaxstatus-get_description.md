---
UID: NF:faxcom.IFaxStatus.get_Description
title: IFaxStatus::get_Description (faxcom.h)
description: Retrieves the Description property for the FaxStatus object of a parent FaxPort object. The Description property is a null-terminated string that describes the current status of the specified port.
helpviewer_keywords: ["Description property [Fax Service]","Description property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","Description property","IFaxStatus.Description","IFaxStatus.get_Description","IFaxStatus::Description","IFaxStatus::get_Description","_mfax_ifaxstatus_get_description","fax._mfax_ifaxstatus_get_description","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_description_cpp","faxcom/IFaxStatus::Description","faxcom/IFaxStatus::get_Description","get_Description"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_description_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5goe.htm
ms.date: 12/05/2018
ms.keywords: Description property [Fax Service], Description property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],Description property, IFaxStatus.Description, IFaxStatus.get_Description, IFaxStatus::Description, IFaxStatus::get_Description, _mfax_ifaxstatus_get_description, fax._mfax_ifaxstatus_get_description, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_description_cpp, faxcom/IFaxStatus::Description, faxcom/IFaxStatus::get_Description, get_Description
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
 - IFaxStatus::get_Description
 - faxcom/IFaxStatus::get_Description
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
 - IFaxStatus.Description
 - IFaxStatus.get_Description
---

# IFaxStatus::get_Description


## -description

Retrieves the <b>Description</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Description</b> property is a null-terminated string that describes the current status of the specified port.

This property is read-only.

## -parameters

## -remarks

If the descriptive information is not available, the <b>IFaxStatus::get_Description</b> method returns an empty string.

The <b>IFaxStatus::get_Description</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>