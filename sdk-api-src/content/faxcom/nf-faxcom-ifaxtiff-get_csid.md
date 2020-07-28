---
UID: NF:faxcom.IFaxTiff.get_Csid
title: IFaxTiff::get_Csid (faxcom.h)
description: Retrieves the Csid property for a FaxTiff object. The Csid property is a string that contains called station identifier (CSID) information, which is typically the fax number of the device that received the specified fax file.
helpviewer_keywords: ["Csid property [Fax Service]","Csid property [Fax Service]","IFaxTiff interface","IFaxTiff interface [Fax Service]","Csid property","IFaxTiff.Csid","IFaxTiff.get_Csid","IFaxTiff::Csid","IFaxTiff::get_Csid","_mfax_ifaxtiff_get_csid","fax._mfax_ifaxtiff_get_csid","fax._mfax_ifaxtiff_mfax_ifaxtiff_get_csid_cpp","faxcom/IFaxTiff::Csid","faxcom/IFaxTiff::get_Csid","get_Csid"]
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_csid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2ask.htm
ms.date: 12/05/2018
ms.keywords: Csid property [Fax Service], Csid property [Fax Service],IFaxTiff interface, IFaxTiff interface [Fax Service],Csid property, IFaxTiff.Csid, IFaxTiff.get_Csid, IFaxTiff::Csid, IFaxTiff::get_Csid, _mfax_ifaxtiff_get_csid, fax._mfax_ifaxtiff_get_csid, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_csid_cpp, faxcom/IFaxTiff::Csid, faxcom/IFaxTiff::get_Csid, get_Csid
f1_keywords:
- faxcom/IFaxTiff.Csid
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Faxcom.dll
api_name:
- IFaxTiff.Csid
- IFaxTiff.get_Csid
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxTiff::get_Csid


## -description


Retrieves the <b>Csid</b> property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object. The <b>Csid</b> property is a string that contains called station identifier (CSID) information, which is typically the fax number of the device that received the specified fax file.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">Image</a> property before retrieving another property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxtiff">FaxTiff</a> object.

The <b>get_Csid</b> method sets the <i>pVal</i> parameter to the string that identifies the called device, if that information is available. If the information is not available, the method returns "Unavailable".

The <b>Csid</b> property is a string that identifies the called device, if that information is available. If the information is not available, <b>Csid</b> is an empty string.

The <b>get_Csid</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxtiff-get-image-vb">IFaxTiff::get_Image</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
 

 

