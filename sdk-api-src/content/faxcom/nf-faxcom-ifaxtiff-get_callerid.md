---
UID: NF:faxcom.IFaxTiff.get_CallerId
title: IFaxTiff::get_CallerId
author: windows-sdk-content
description: Retrieves the CallerId property for a FaxTiff object. The CallerId property is a string that identifies the calling device that sent a specified fax file.
old-location: fax\_mfax_ifaxtiff_get_callerid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_502s.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CallerId property [Fax Service], CallerId property [Fax Service],FaxTiff object, FaxTiff object [Fax Service],CallerId property, FaxTiff.CallerId, IFaxTiff.get_CallerId, IFaxTiff::get_CallerId, _mfax_ifaxtiff_get_callerid, fax._mfax_ifaxtiff_get_callerid, fax._mfax_ifaxtiff_get_callerid_vb, get_CallerId
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
 - FaxTiff.CallerId
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxTiff::get_CallerId


## -description


Retrieves the <b>CallerId</b> property for a <a href="https://msdn.microsoft.com/library/ms691832(v=VS.85).aspx">FaxTiff</a> object. The <b>CallerId</b> property is a string that identifies the calling device that sent a specified fax file.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://msdn.microsoft.com/9e41ae1f-070d-4365-9d6a-a37f1979dae7">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/library/ms691832(v=VS.85).aspx">FaxTiff</a> object.

The <b>get_CallerId</b> method sets the <i>pVal</i> parameter to the string that identifies the calling device, if it is available. If the information is not available, the method returns "Unavailable".

The <b>CallerId</b> property is a string that identifies the calling device, if it is available. If the information is not available, <b>CallerId</b> is an empty string.

The <b>get_CallerId</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690285(v=VS.85).aspx">FaxTiff</a>



<a href="https://msdn.microsoft.com/library/ms691802(v=VS.85).aspx">IFaxTiff</a>



<a href="https://msdn.microsoft.com/9e41ae1f-070d-4365-9d6a-a37f1979dae7">Image</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

