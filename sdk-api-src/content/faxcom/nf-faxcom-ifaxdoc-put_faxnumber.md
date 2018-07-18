---
UID: NF:faxcom.IFaxDoc.put_FaxNumber
title: IFaxDoc::put_FaxNumber
author: windows-sdk-content
description: Sets or retrieves the FaxNumber property of a FaxDoc object. The FaxNumber property is a null-terminated string that contains the fax number to which the fax server will send the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_faxnumber_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_833m.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxDoc object [Fax Service],FaxNumber property, FaxDoc.FaxNumber, FaxNumber property [Fax Service], FaxNumber property [Fax Service],FaxDoc object, IFaxDoc.put_FaxNumber, IFaxDoc::put_FaxNumber, _mfax_ifaxdoc_get_faxnumber, fax._mfax_ifaxdoc_get_faxnumber, fax._mfax_ifaxdoc_get_faxnumber_vb, put_FaxNumber
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxDoc.FaxNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::put_FaxNumber


## -description


Sets or retrieves the <b>FaxNumber</b> property of a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>FaxNumber</b> property is a null-terminated string that contains the fax number to which the fax server will send the fax transmission.

This property is read/write.


## -parameters


## -remarks



The recipient's fax number can appear on the cover page. 

The <b>FaxNumber</b> property is required to send a fax transmission using a call to the <a href="https://msdn.microsoft.com/library/ms692792(v=VS.85).aspx">Send</a> method. For more information, see <a href="https://msdn.microsoft.com/library/ms691959(v=VS.85).aspx">Transmitting Faxes</a>.

The <b>FaxNumber</b> property is required to send a fax transmission using a call to the <a href="https://msdn.microsoft.com/library/ms692792(v=VS.85).aspx">Send</a> method. For more information, see <a href="https://msdn.microsoft.com/library/ms691959(v=VS.85).aspx">Transmitting Faxes</a>.

The <b>get_FaxNumber</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690707(v=VS.85).aspx">FaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms692792(v=VS.85).aspx">Send</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

