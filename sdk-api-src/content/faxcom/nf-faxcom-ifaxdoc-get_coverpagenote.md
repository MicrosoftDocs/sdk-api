---
UID: NF:faxcom.IFaxDoc.get_CoverpageNote
title: IFaxDoc::get_CoverpageNote (faxcom.h)
description: Sets or retrieves the CoverpageNote property of a FaxDoc object. The CoverpageNote property is a null-terminated string that contains the text of a message or note from the sender that pertains to the fax transmission. (Get)
helpviewer_keywords: ["CoverpageNote property [Fax Service]","CoverpageNote property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","CoverpageNote property","IFaxDoc.CoverpageNote","IFaxDoc.get_CoverpageNote","IFaxDoc::CoverpageNote","IFaxDoc::get_CoverpageNote","IFaxDoc::put_CoverpageNote","_mfax_ifaxdoc_get_coverpagenote","fax._mfax_ifaxdoc_get_coverpagenote","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagenote_cpp","faxcom/IFaxDoc::CoverpageNote","faxcom/IFaxDoc::get_CoverpageNote","faxcom/IFaxDoc::put_CoverpageNote","get_CoverpageNote"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagenote_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4t7p.htm
ms.date: 12/05/2018
ms.keywords: CoverpageNote property [Fax Service], CoverpageNote property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],CoverpageNote property, IFaxDoc.CoverpageNote, IFaxDoc.get_CoverpageNote, IFaxDoc::CoverpageNote, IFaxDoc::get_CoverpageNote, IFaxDoc::put_CoverpageNote, _mfax_ifaxdoc_get_coverpagenote, fax._mfax_ifaxdoc_get_coverpagenote, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagenote_cpp, faxcom/IFaxDoc::CoverpageNote, faxcom/IFaxDoc::get_CoverpageNote, faxcom/IFaxDoc::put_CoverpageNote, get_CoverpageNote
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
 - IFaxDoc::get_CoverpageNote
 - faxcom/IFaxDoc::get_CoverpageNote
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
 - IFaxDoc.CoverpageNote
 - IFaxDoc.get_CoverpageNote
 - IFaxDoc.put_CoverpageNote
---

# IFaxDoc::get_CoverpageNote


## -description

Sets or retrieves the <b>CoverpageNote</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>CoverpageNote</b> property is a null-terminated string that contains the text of a message or note from the sender that pertains to the fax transmission.

This property is read/write.

## -parameters

## -remarks

The cover page note can appear on the cover page.

The <b>get_CoverpageNote</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
