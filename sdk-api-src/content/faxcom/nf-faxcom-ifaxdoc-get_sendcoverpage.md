---
UID: NF:faxcom.IFaxDoc.get_SendCoverpage
title: IFaxDoc::get_SendCoverpage
author: windows-sdk-content
description: Sets or retrieves the SendCoverpage property for a FaxDoc object. The SendCoverpage property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.
old-location: fax\_mfax_ifaxdoc_get_sendcoverpage_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1yud.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FaxDoc object [Fax Service],SendCoverpage property, FaxDoc.SendCoverpage, IFaxDoc.get_SendCoverpage, IFaxDoc::get_SendCoverpage, SendCoverpage property [Fax Service], SendCoverpage property [Fax Service],FaxDoc object, _mfax_ifaxdoc_get_sendcoverpage, fax._mfax_ifaxdoc_get_sendcoverpage, fax._mfax_ifaxdoc_get_sendcoverpage_vb, get_SendCoverpage
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
 - FaxDoc.SendCoverpage
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::get_SendCoverpage


## -description


Sets or retrieves the <b>SendCoverpage</b> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SendCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

This property is read/write.


## -parameters


## -remarks



To send a cover page with a fax document, the following are required:
		        

<ul>
<li>The <b>SendCoverpage</b> property must be equal to <b>True</b>.</li>
<li>The <b>CoverpageName</b> property must specify a valid cover page file.</li>
</ul>
In addition, the <a href="https://msdn.microsoft.com/86895798-9451-40a8-95e0-35bab5871ede">ServerCoverpage</a> property must be equal to <b>True</b> if the cover page file is a common cover page file. For more information, see <a href="https://msdn.microsoft.com/6d2fbcb1-fb94-4fe1-8481-f64f55878906">CoverpageName</a>.

You can call the <a href="https://msdn.microsoft.com/b8e22223-eada-44b6-9a84-45b5a29f6eb2">ServerCoverpage</a> method to determine whether the fax server is configured to permit personal cover pages.

The <b>SendCoverpage</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.

For more information, see <a href="https://msdn.microsoft.com/37bbff77-08a8-486f-ac26-d7b69a936e05">Cover Pages</a> and <a href="https://msdn.microsoft.com/32e293c8-febb-43c0-801c-f7b4a6675c80">Sending a Cover Page</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/6bf5be89-efc8-41e7-bde9-0c0ba7f0e61c">FaxDoc</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922788">FileName</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>



<a href="https://msdn.microsoft.com/86895798-9451-40a8-95e0-35bab5871ede">ServerCoverpage</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
 

 

