---
UID: NF:faxcom.IFaxDoc.put_SenderOfficePhone
title: IFaxDoc::put_SenderOfficePhone
author: windows-sdk-content
description: Sets or retrieves the SenderOfficePhone property of a FaxDoc object. The SenderOfficePhone property is a null-terminated string that contains the office telephone number of the sender of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_senderofficephone_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0mzp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxDoc interface [Fax Service],SenderOfficePhone property, IFaxDoc.SenderOfficePhone, IFaxDoc.put_SenderOfficePhone, IFaxDoc::SenderOfficePhone, IFaxDoc::get_SenderOfficePhone, IFaxDoc::put_SenderOfficePhone, SenderOfficePhone property [Fax Service], SenderOfficePhone property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_senderofficephone, fax._mfax_ifaxdoc_get_senderofficephone, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_senderofficephone_cpp, faxcom/IFaxDoc::SenderOfficePhone, faxcom/IFaxDoc::get_SenderOfficePhone, faxcom/IFaxDoc::put_SenderOfficePhone, put_SenderOfficePhone
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFaxDoc.SenderOfficePhone
 - IFaxDoc.get_SenderOfficePhone
 - IFaxDoc.put_SenderOfficePhone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_SenderOfficePhone


## -description


Sets or retrieves the <b>SenderOfficePhone</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderOfficePhone</b> property is a null-terminated string that contains the office telephone number of the sender of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax sender's office telephone number can appear on the cover page.

The <b>IFaxDoc::get_SenderOfficePhone</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

