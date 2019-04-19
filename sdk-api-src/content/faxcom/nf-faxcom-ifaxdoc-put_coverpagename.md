---
UID: NF:faxcom.IFaxDoc.put_CoverpageName
title: IFaxDoc::put_CoverpageName (faxcom.h)
author: windows-sdk-content
description: Sets or retrieves the CoverpageName property for a FaxDoc object. The CoverpageName property is a null-terminated string that contains the name of the cover page template file (.cov) associated with the object.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3kmd.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoverpageName property [Fax Service], CoverpageName property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],CoverpageName property, IFaxDoc.CoverpageName, IFaxDoc.put_CoverpageName, IFaxDoc::CoverpageName, IFaxDoc::get_CoverpageName, IFaxDoc::put_CoverpageName, _mfax_ifaxdoc_get_coverpagename, fax._mfax_ifaxdoc_get_coverpagename, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_coverpagename_cpp, faxcom/IFaxDoc::CoverpageName, faxcom/IFaxDoc::get_CoverpageName, faxcom/IFaxDoc::put_CoverpageName, put_CoverpageName
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
 - IFaxDoc.CoverpageName
 - IFaxDoc.get_CoverpageName
 - IFaxDoc.put_CoverpageName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDoc::put_CoverpageName


## -description


Sets or retrieves the <b>CoverpageName</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>CoverpageName</b> property is a null-terminated string that contains the name of the cover page template file (.cov) associated with the object.

This property is read/write.


## -parameters


## -remarks



To send a cover page with a fax document, the following are required:
		        

<ul>
<li>The <b>SendCoverpage</b> property must be equal to <b>TRUE</b>.</li>
<li>The <b>CoverpageName</b> property must specify a valid cover page file.</li>
</ul>
In addition, the <a href="https://msdn.microsoft.com/en-us/library/ms690883(v=VS.85).aspx">ServerCoverpage</a> property must be equal to <b>TRUE</b> if the cover page file is a common cover page file. 

You can call the <a href="https://msdn.microsoft.com/en-us/library/ms691428(v=VS.85).aspx">ServerCoverpage</a> method to determine whether the fax server is configured to permit personal cover pages.

The <b>IFaxDoc::get_CoverpageName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691363(v=VS.85).aspx">Cover Pages</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690892(v=VS.85).aspx">Sending a Cover Page</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692340(v=VS.85).aspx">IFaxDoc::get_FileName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690883(v=VS.85).aspx">IFaxDoc::get_ServerCoverpage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

