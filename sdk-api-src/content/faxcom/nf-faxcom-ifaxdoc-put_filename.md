---
UID: NF:faxcom.IFaxDoc.put_FileName
title: IFaxDoc::put_FileName (faxcom.h)
description: Sets or retrieves the FileName property for a FaxDoc object. The FileName property is a null-terminated string that contains the name of the document file associated with the object. (Put)
helpviewer_keywords: ["FileName property [Fax Service]","FileName property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","FileName property","IFaxDoc.FileName","IFaxDoc.put_FileName","IFaxDoc::FileName","IFaxDoc::get_FileName","IFaxDoc::put_FileName","_mfax_ifaxdoc_get_filename","fax._mfax_ifaxdoc_get_filename","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_filename_cpp","faxcom/IFaxDoc::FileName","faxcom/IFaxDoc::get_FileName","faxcom/IFaxDoc::put_FileName","put_FileName"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_filename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7rqd.htm
ms.date: 12/05/2018
ms.keywords: FileName property [Fax Service], FileName property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],FileName property, IFaxDoc.FileName, IFaxDoc.put_FileName, IFaxDoc::FileName, IFaxDoc::get_FileName, IFaxDoc::put_FileName, _mfax_ifaxdoc_get_filename, fax._mfax_ifaxdoc_get_filename, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_filename_cpp, faxcom/IFaxDoc::FileName, faxcom/IFaxDoc::get_FileName, faxcom/IFaxDoc::put_FileName, put_FileName
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
 - IFaxDoc::put_FileName
 - faxcom/IFaxDoc::put_FileName
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
 - IFaxDoc.FileName
 - IFaxDoc.get_FileName
 - IFaxDoc.put_FileName
---

# IFaxDoc::put_FileName


## -description

Sets or retrieves the <b>FileName</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>FileName</b> property is a null-terminated string that contains the name of the document file associated with the object.

This property is read/write.

## -parameters

## -remarks

The <b>FileName</b> property is required to send a fax transmission using a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">IFaxDoc::Send</a> method. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-transmitting-faxes">Transmitting Faxes</a>.

The <b>get_FileName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
