---
UID: NF:faxcom.IFaxDoc.put_Tsid
title: IFaxDoc::put_Tsid (faxcom.h)
description: Sets or retrieves the Tsid property of a FaxDoc object. The Tsid property is a null-terminated string that contains a user-defined transmitting station identifier (TSID). (Put)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","Tsid property","IFaxDoc.Tsid","IFaxDoc.put_Tsid","IFaxDoc::Tsid","IFaxDoc::get_Tsid","IFaxDoc::put_Tsid","Tsid property [Fax Service]","Tsid property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_tsid","fax._mfax_ifaxdoc_get_tsid","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_tsid_cpp","faxcom/IFaxDoc::Tsid","faxcom/IFaxDoc::get_Tsid","faxcom/IFaxDoc::put_Tsid","put_Tsid"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3xyc.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],Tsid property, IFaxDoc.Tsid, IFaxDoc.put_Tsid, IFaxDoc::Tsid, IFaxDoc::get_Tsid, IFaxDoc::put_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_tsid, fax._mfax_ifaxdoc_get_tsid, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_tsid_cpp, faxcom/IFaxDoc::Tsid, faxcom/IFaxDoc::get_Tsid, faxcom/IFaxDoc::put_Tsid, put_Tsid
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
 - IFaxDoc::put_Tsid
 - faxcom/IFaxDoc::put_Tsid
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
 - IFaxDoc.Tsid
 - IFaxDoc.get_Tsid
 - IFaxDoc.put_Tsid
---

# IFaxDoc::put_Tsid


## -description

Sets or retrieves the <b>Tsid</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>Tsid</b> property is a null-terminated string that contains a user-defined transmitting station identifier (TSID).

This property is read/write.

## -parameters

## -remarks

If the fax server allows user-defined TSID strings, the service will transmit the value of the <i>pVal</i> parameter to the receiving fax device instead of the TSID associated with the sending device. You can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-usedevicetsid-vb">UseDeviceTsid</a> method to determine whether the fax server is configured to permit user-specified TSIDs.

If the fax server allows user-defined TSID strings, the service will transmit the value of <i>pVal</i> to the receiving fax device instead of the TSID associated with the sending device. You can use the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-usedevicetsid-vb">UseDeviceTsid</a> property to determine whether the fax server is configured to permit user-specified TSIDs.

The TSID is typically the fax number of the device sending the transmission. Note that the T.30 specification of the International Telecommunication Union (ITU) restricts the value of a TSID to 20 ASCII characters. If a fax client application specifies a TSID that contains non-ASCII characters, the fax service removes them. If the TSID exceeds 20 characters, the service truncates the extra characters.

The <b>get_Tsid</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-usedevicetsid-vb">UseDeviceTsid</a>
