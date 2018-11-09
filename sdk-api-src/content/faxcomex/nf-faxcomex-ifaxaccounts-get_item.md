---
UID: NF:faxcomex.IFaxAccounts.get_Item
title: IFaxAccounts::get_Item
author: windows-sdk-content
description: Returns a FaxAccount object from a FaxAccounts collection.
old-location: fax\_mfax_faxaccounts_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccounts\get_item.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxAccounts interface [Fax Service],get_Item method, IFaxAccounts.get_Item, IFaxAccounts::get_Item, _mfax_faxaccounts.item_cpp, fax._mfax_faxaccounts_item_cpp, faxcomex/IFaxAccounts::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxAccounts interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxAccounts.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccounts::get_Item


## -description


Returns a <a href="https://msdn.microsoft.com/en-us/library/Aa358967(v=VS.85).aspx">FaxAccount</a> object from a <a href="https://msdn.microsoft.com/en-us/library/Aa358940(v=VS.85).aspx">FaxAccounts</a> collection. 


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies a value that indicates the item to retrieve from the collection. If this parameter is type <b>VT_I2</b> or <b>VT_I4</b>, it specifies the index of the item to retrieve. The index is 1-based. If this parameter is type <b>VT_BSTR</b>, it specifies the account name to use to search the collection. Other types are not supported. 


### -param pFaxAccount

TBD




#### - ppFaxAccount [out, retval]

Type: <b><a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a>**</b>

The <a href="https://msdn.microsoft.com/en-us/library/Aa358967(v=VS.85).aspx">FaxAccount</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa359019(v=VS.85).aspx">IFaxAccounts</a>



<a href="https://msdn.microsoft.com/eab831e4-a260-4822-8582-532f7717dab8">Item</a>
 

 

