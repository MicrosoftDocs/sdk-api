---
UID: NF:faxcom.IFaxDoc.put_RecipientCountry
title: IFaxDoc::put_RecipientCountry
author: windows-sdk-content
description: Sets or retrieves the RecipientCountry property of a FaxDoc object. The RecipientCountry property is a null-terminated string that contains the country/region of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcountry_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7ybd.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientCountry property, IFaxDoc.RecipientCountry, IFaxDoc.put_RecipientCountry, IFaxDoc::RecipientCountry, IFaxDoc::get_RecipientCountry, IFaxDoc::put_RecipientCountry, RecipientCountry property [Fax Service], RecipientCountry property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientcountry, fax._mfax_ifaxdoc_get_recipientcountry, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcountry_cpp, faxcom/IFaxDoc::RecipientCountry, faxcom/IFaxDoc::get_RecipientCountry, faxcom/IFaxDoc::put_RecipientCountry, put_RecipientCountry
ms.topic: method
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
 - IFaxDoc.RecipientCountry
 - IFaxDoc.get_RecipientCountry
 - IFaxDoc.put_RecipientCountry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_RecipientCountry


## -description


Sets or retrieves the <b>RecipientCountry</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientCountry</b> property is a null-terminated string that contains the country/region of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's country/region name can appear on the cover page.

The <b>get_RecipientCountry</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

