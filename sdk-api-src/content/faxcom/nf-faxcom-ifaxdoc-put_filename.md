---
UID: NF:faxcom.IFaxDoc.put_FileName
title: IFaxDoc::put_FileName
author: windows-sdk-content
description: Sets or retrieves the FileName property for a FaxDoc object. The FileName property is a null-terminated string that contains the name of the document file associated with the object.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_filename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7rqd.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FileName property [Fax Service], FileName property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],FileName property, IFaxDoc.FileName, IFaxDoc.put_FileName, IFaxDoc::FileName, IFaxDoc::get_FileName, IFaxDoc::put_FileName, _mfax_ifaxdoc_get_filename, fax._mfax_ifaxdoc_get_filename, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_filename_cpp, faxcom/IFaxDoc::FileName, faxcom/IFaxDoc::get_FileName, faxcom/IFaxDoc::put_FileName, put_FileName
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
 - IFaxDoc.FileName
 - IFaxDoc.get_FileName
 - IFaxDoc.put_FileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_FileName


## -description


Sets or retrieves the <b>FileName</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>FileName</b> property is a null-terminated string that contains the name of the document file associated with the object.

This property is read/write.


## -parameters


## -remarks



The <b>FileName</b> property is required to send a fax transmission using a call to the <a href="https://msdn.microsoft.com/a4c70429-4d1d-4708-acd6-e077bddfbd6c">IFaxDoc::Send</a> method. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691959(v=VS.85).aspx">Transmitting Faxes</a>.

The <b>get_FileName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

