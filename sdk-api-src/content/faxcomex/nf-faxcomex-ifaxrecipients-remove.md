---
UID: NF:faxcomex.IFaxRecipients.Remove
title: IFaxRecipients::Remove (faxcomex.h)
description: The IFaxRecipients::Remove method removes an item from the FaxRecipients collection.
helpviewer_keywords: ["IFaxRecipients interface [Fax Service]","Remove method","IFaxRecipients.Remove","IFaxRecipients::Remove","Remove","Remove method [Fax Service]","Remove method [Fax Service]","IFaxRecipients interface","_mfax_faxrecipients.remove","fax._mfax_faxrecipients_cpp_mfax_faxrecipients_remove_cpp","fax._mfax_faxrecipients_remove","faxcomex/IFaxRecipients::Remove"]
old-location: fax\_mfax_faxrecipients_cpp_mfax_faxrecipients_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9c9x.htm
ms.date: 12/05/2018
ms.keywords: IFaxRecipients interface [Fax Service],Remove method, IFaxRecipients.Remove, IFaxRecipients::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxRecipients interface, _mfax_faxrecipients.remove, fax._mfax_faxrecipients_cpp_mfax_faxrecipients_remove_cpp, fax._mfax_faxrecipients_remove, faxcomex/IFaxRecipients::Remove
f1_keywords:
- faxcomex/IFaxRecipients.Remove
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxRecipients::Remove


## -description


The <b>IFaxRecipients::Remove</b> method removes an item from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> collection.


## -parameters




### -param lIndex [out, retval]

Type: <b>LONG</b>

A <b>LONG</b> that specifies the index of the item to remove from the collection. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of recipients returned by a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients-count-vb">IFaxRecipients::get_Count</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-broadcasting-a-fax">Broadcasting a Fax</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxrecipients">IFaxRecipients</a>
 

 

