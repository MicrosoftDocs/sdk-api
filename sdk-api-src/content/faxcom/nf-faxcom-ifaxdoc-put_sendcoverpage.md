---
UID: NF:faxcom.IFaxDoc.put_SendCoverpage
title: IFaxDoc::put_SendCoverpage (faxcom.h)
description: Sets or retrieves the SendCoverpage property for a FaxDoc object. The SendCoverpage property is a Boolean value that indicates whether the specified cover page file is stored on the fax server. (Put)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","SendCoverpage property","IFaxDoc.SendCoverpage","IFaxDoc.put_SendCoverpage","IFaxDoc::SendCoverpage","IFaxDoc::get_SendCoverpage","IFaxDoc::put_SendCoverpage","SendCoverpage property [Fax Service]","SendCoverpage property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_sendcoverpage","fax._mfax_ifaxdoc_get_sendcoverpage","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_sendcoverpage_cpp","faxcom/IFaxDoc::SendCoverpage","faxcom/IFaxDoc::get_SendCoverpage","faxcom/IFaxDoc::put_SendCoverpage","put_SendCoverpage"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_sendcoverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1yud.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],SendCoverpage property, IFaxDoc.SendCoverpage, IFaxDoc.put_SendCoverpage, IFaxDoc::SendCoverpage, IFaxDoc::get_SendCoverpage, IFaxDoc::put_SendCoverpage, SendCoverpage property [Fax Service], SendCoverpage property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_sendcoverpage, fax._mfax_ifaxdoc_get_sendcoverpage, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_sendcoverpage_cpp, faxcom/IFaxDoc::SendCoverpage, faxcom/IFaxDoc::get_SendCoverpage, faxcom/IFaxDoc::put_SendCoverpage, put_SendCoverpage
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
 - IFaxDoc::put_SendCoverpage
 - faxcom/IFaxDoc::put_SendCoverpage
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
 - IFaxDoc.SendCoverpage
 - IFaxDoc.get_SendCoverpage
 - IFaxDoc.put_SendCoverpage
---

# IFaxDoc::put_SendCoverpage


## -description

Sets or retrieves the <b>SendCoverpage</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SendCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

This property is read/write.

## -parameters

## -remarks

To send a cover page with a fax document, the following are required:
		        

<ul>
<li>The <b>SendCoverpage</b> property must be equal to <b>TRUE</b>.</li>
<li>The <b>CoverpageName</b> property must specify a valid cover page file.</li>
</ul>
In addition, the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-servercoverpage-vb">ServerCoverpage</a> property must be equal to <b>TRUE</b> if the cover page file is a common cover page file. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-coverpagename-vb">CoverpageName</a>.

You can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-servercoverpage-vb">ServerCoverpage</a> method to determine whether the fax server is configured to permit personal cover pages.

The <b>IFaxDoc::get_SendCoverpage</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-cover-pages">Cover Pages</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-cover-page">Sending a Cover Page</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">IFaxDoc::get_FileName</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-servercoverpage-vb">IFaxDoc::get_ServerCoverpage</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
