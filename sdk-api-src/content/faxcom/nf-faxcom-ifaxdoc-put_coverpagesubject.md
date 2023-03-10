---
UID: NF:faxcom.IFaxDoc.put_CoverpageSubject
title: IFaxDoc::put_CoverpageSubject (faxcom.h)
description: Sets or retrieves the CoverpageSubject property of a FaxDoc object. The CoverpageSubject property is a null-terminated string that contains the subject line of the fax transmission. (Put)
helpviewer_keywords: ["CoverpageSubject property [Fax Service]","CoverpageSubject property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","CoverpageSubject property","IFaxDoc.CoverpageSubject","IFaxDoc.put_CoverpageSubject","IFaxDoc::CoverpageSubject","IFaxDoc::get_CoverpageSubject","IFaxDoc::put_CoverpageSubject","_mfax_ifaxdoc_get_coverpagesubject","fax._mfax_ifaxdoc_get_coverpagesubject","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagesubject_cpp","faxcom/IFaxDoc::CoverpageSubject","faxcom/IFaxDoc::get_CoverpageSubject","faxcom/IFaxDoc::put_CoverpageSubject","put_CoverpageSubject"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagesubject_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6svo.htm
ms.date: 12/05/2018
ms.keywords: CoverpageSubject property [Fax Service], CoverpageSubject property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],CoverpageSubject property, IFaxDoc.CoverpageSubject, IFaxDoc.put_CoverpageSubject, IFaxDoc::CoverpageSubject, IFaxDoc::get_CoverpageSubject, IFaxDoc::put_CoverpageSubject, _mfax_ifaxdoc_get_coverpagesubject, fax._mfax_ifaxdoc_get_coverpagesubject, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagesubject_cpp, faxcom/IFaxDoc::CoverpageSubject, faxcom/IFaxDoc::get_CoverpageSubject, faxcom/IFaxDoc::put_CoverpageSubject, put_CoverpageSubject
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
 - IFaxDoc::put_CoverpageSubject
 - faxcom/IFaxDoc::put_CoverpageSubject
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
 - IFaxDoc.CoverpageSubject
 - IFaxDoc.get_CoverpageSubject
 - IFaxDoc.put_CoverpageSubject
---

# IFaxDoc::put_CoverpageSubject


## -description

Sets or retrieves the <b>CoverpageSubject</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>CoverpageSubject</b> property is a null-terminated string that contains the subject line of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The cover page subject can appear on the cover page.

The <b>get_CoverpageSubject</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
