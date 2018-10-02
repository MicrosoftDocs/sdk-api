---
UID: NF:faxcom.IFaxDoc.put_SendCoverpage
title: IFaxDoc::put_SendCoverpage
author: windows-sdk-content
description: Sets or retrieves the SendCoverpage property for a FaxDoc object. The SendCoverpage property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_sendcoverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1yud.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxDoc interface [Fax Service],SendCoverpage property, IFaxDoc.SendCoverpage, IFaxDoc.put_SendCoverpage, IFaxDoc::SendCoverpage, IFaxDoc::get_SendCoverpage, IFaxDoc::put_SendCoverpage, SendCoverpage property [Fax Service], SendCoverpage property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_sendcoverpage, fax._mfax_ifaxdoc_get_sendcoverpage, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_sendcoverpage_cpp, faxcom/IFaxDoc::SendCoverpage, faxcom/IFaxDoc::get_SendCoverpage, faxcom/IFaxDoc::put_SendCoverpage, put_SendCoverpage
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
 - IFaxDoc.SendCoverpage
 - IFaxDoc.get_SendCoverpage
 - IFaxDoc.put_SendCoverpage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_SendCoverpage


## -description


Sets or retrieves the <b>SendCoverpage</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SendCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

This property is read/write.


## -parameters


## -remarks



To send a cover page with a fax document, the following are required:
		        

<ul>
<li>The <b>SendCoverpage</b> property must be equal to <b>TRUE</b>.</li>
<li>The <b>CoverpageName</b> property must specify a valid cover page file.</li>
</ul>
In addition, the <a href="https://msdn.microsoft.com/c7571a29-c145-4ab6-976e-547f9491cf1f">ServerCoverpage</a> property must be equal to <b>TRUE</b> if the cover page file is a common cover page file. For more information, see <a href="https://msdn.microsoft.com/b15a818b-fd37-4958-8fc7-25a8494cdf12">CoverpageName</a>.

You can call the <a href="https://msdn.microsoft.com/889e7233-fe5b-41f9-8436-0c7b28d78653">ServerCoverpage</a> method to determine whether the fax server is configured to permit personal cover pages.

The <b>IFaxDoc::get_SendCoverpage</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691363(v=VS.85).aspx">Cover Pages</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690892(v=VS.85).aspx">Sending a Cover Page</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/fe9f0c64-7722-49ca-809c-5e59acacf474">IFaxDoc::get_FileName</a>



<a href="https://msdn.microsoft.com/c7571a29-c145-4ab6-976e-547f9491cf1f">IFaxDoc::get_ServerCoverpage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

