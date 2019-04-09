---
UID: NF:faxcomex.IFaxRecipients.Remove
title: IFaxRecipients::Remove (faxcomex.h)
author: windows-sdk-content
description: The IFaxRecipients::Remove method removes an item from the FaxRecipients collection.
old-location: fax\_mfax_faxrecipients_cpp_mfax_faxrecipients_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9c9x.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxRecipients interface [Fax Service],Remove method, IFaxRecipients.Remove, IFaxRecipients::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxRecipients interface, _mfax_faxrecipients.remove, fax._mfax_faxrecipients_cpp_mfax_faxrecipients_remove_cpp, fax._mfax_faxrecipients_remove, faxcomex/IFaxRecipients::Remove
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
 - IFaxRecipients.Remove
 - IFaxRecipients.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRecipients::Remove


## -description


The <b>IFaxRecipients::Remove</b> method removes an item from the <a href="https://msdn.microsoft.com/en-us/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection.


## -parameters




### -param lIndex [out, retval]

Type: <b>LONG</b>

A <b>LONG</b> that specifies the index of the item to remove from the collection. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of recipients returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms688447(v=VS.85).aspx">IFaxRecipients::get_Count</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693479(v=VS.85).aspx">Broadcasting a Fax</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689604(v=VS.85).aspx">FaxRecipients</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689605(v=VS.85).aspx">IFaxRecipients</a>
 

 

