---
UID: NF:faxcomex.IFaxRecipients.Add
title: IFaxRecipients::Add (faxcomex.h)
author: windows-sdk-content
description: The IFaxRecipients::Add method adds a new FaxRecipient object to the FaxRecipients collection.
old-location: fax\_mfax_faxrecipients_cpp_mfax_faxrecipients_add_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_73l0.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxRecipients interface, IFaxRecipients interface [Fax Service],Add method, IFaxRecipients.Add, IFaxRecipients::Add, _mfax_faxrecipients.add, fax._mfax_faxrecipients_add, fax._mfax_faxrecipients_cpp_mfax_faxrecipients_add_cpp, faxcomex/IFaxRecipients::Add
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxRecipients.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxRecipients::Add


## -description


The <b>IFaxRecipients::Add</b> method adds a new <a href="https://msdn.microsoft.com/en-us/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object to the <a href="https://msdn.microsoft.com/en-us/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection. 


## -parameters




### -param bstrFaxNumber

Type: <b>BSTR</b>

Specifies the fax number of the fax recipient.


### -param bstrRecipientName [optional]

Type: <b>BSTR</b>

Specifies the name of the fax recipient. 


### -param ppFaxRecipient [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms690206(v=VS.85).aspx">IFaxRecipient</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693479(v=VS.85).aspx">Broadcasting a Fax</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689604(v=VS.85).aspx">FaxRecipients</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689605(v=VS.85).aspx">IFaxRecipients</a>
 

 

