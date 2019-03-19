---
UID: NF:faxcomex.IFaxRecipients.get_Item
title: IFaxRecipients::get_Item (faxcomex.h)
author: windows-sdk-content
description: The Item method returns a FaxRecipient object from the FaxRecipients collection.
old-location: fax\_mfax_faxrecipients_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0q7h_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxRecipients interface [Fax Service],get_Item method, IFaxRecipients.get_Item, IFaxRecipients::get_Item, _mfax_faxrecipients.item_cpp, fax._mfax_faxrecipients_item_cpp, faxcomex/IFaxRecipients::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxRecipients interface
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
 - IFaxRecipients.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRecipients::get_Item


## -description


The <a href="https://msdn.microsoft.com/en-us/library/ms687542(v=VS.85).aspx">Item</a> method returns a <a href="https://msdn.microsoft.com/en-us/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object from the <a href="https://msdn.microsoft.com/en-us/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection. 


## -parameters




### -param lIndex [in]

Type: <b>LONG</b>

A <b>LONG</b> value that specifies the item to retrieve from the fax recipient collection. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of recipients returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms688447(v=VS.85).aspx">IFaxRecipients::get_Count</a> method. 


### -param ppFaxRecipient [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms690206(v=VS.85).aspx">IFaxRecipient</a>**</b>

Address of a pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms690206(v=VS.85).aspx">IFaxRecipient</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693479(v=VS.85).aspx">Broadcasting a Fax</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689604(v=VS.85).aspx">FaxRecipients</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689605(v=VS.85).aspx">IFaxRecipients</a>
 

 

