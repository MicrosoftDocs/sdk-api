---
UID: NF:faxcom.IFaxDoc.put_DisplayName
title: IFaxDoc::put_DisplayName (faxcom.h)
description: Sets or retrieves the DisplayName property of a FaxDoc object. The DisplayName property is a null-terminated string that contains the name to associate with the fax document. (Put)
helpviewer_keywords: ["DisplayName property [Fax Service]","DisplayName property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","DisplayName property","IFaxDoc.DisplayName","IFaxDoc.put_DisplayName","IFaxDoc::DisplayName","IFaxDoc::get_DisplayName","IFaxDoc::put_DisplayName","_mfax_ifaxdoc_get_displayname","fax._mfax_ifaxdoc_get_displayname","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_displayname_cpp","faxcom/IFaxDoc::DisplayName","faxcom/IFaxDoc::get_DisplayName","faxcom/IFaxDoc::put_DisplayName","put_DisplayName"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_displayname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4s6d.htm
ms.date: 12/05/2018
ms.keywords: DisplayName property [Fax Service], DisplayName property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],DisplayName property, IFaxDoc.DisplayName, IFaxDoc.put_DisplayName, IFaxDoc::DisplayName, IFaxDoc::get_DisplayName, IFaxDoc::put_DisplayName, _mfax_ifaxdoc_get_displayname, fax._mfax_ifaxdoc_get_displayname, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_displayname_cpp, faxcom/IFaxDoc::DisplayName, faxcom/IFaxDoc::get_DisplayName, faxcom/IFaxDoc::put_DisplayName, put_DisplayName
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
 - IFaxDoc::put_DisplayName
 - faxcom/IFaxDoc::put_DisplayName
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
 - IFaxDoc.DisplayName
 - IFaxDoc.get_DisplayName
 - IFaxDoc.put_DisplayName
---

# IFaxDoc::put_DisplayName


## -description

Sets or retrieves the <b>DisplayName</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>DisplayName</b> property is a null-terminated string that contains the name to associate with the fax document.

This property is read/write.

## -parameters

## -remarks

The <b>get_DisplayName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
