---
UID: NF:faxcomex.IFaxAccountSet.GetAccounts
title: IFaxAccountSet::GetAccounts
author: windows-sdk-content
description: Returns an IFaxAccounts object that represents all the fax accounts on the fax server.
old-location: fax\_mfax_faxaccountset_cpp_mfax_faxaccountset_getaccounts_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\getaccounts.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GetAccounts, GetAccounts method [Fax Service], GetAccounts method [Fax Service],IFaxAccountSet interface, IFaxAccountSet interface [Fax Service],GetAccounts method, IFaxAccountSet.GetAccounts, IFaxAccountSet::GetAccounts, _mfax_faxaccountset.getaccounts, fax._mfax_faxaccountset_cpp_mfax_faxaccountset_getaccounts_cpp, fax._mfax_faxaccountset_getaccounts, faxcomex/IFaxAccountSet::GetAccounts
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
 - IFaxAccountSet.GetAccounts
 - IFaxAccountSet.GetAccounts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxAccountSet.GetAccounts
: 
---

# IFaxAccountSet::GetAccounts


## -description


Returns an <a href="https://msdn.microsoft.com/73210bf5-cae8-4fea-802a-a37f59a1dd2f">IFaxAccounts</a> object that represents all the fax accounts on the fax server.


## -parameters




### -param ppFaxAccounts [out, retval]

Type: <b><a href="https://msdn.microsoft.com/73210bf5-cae8-4fea-802a-a37f59a1dd2f">IFaxAccounts</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/73210bf5-cae8-4fea-802a-a37f59a1dd2f">IFaxAccounts</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ae298925-c428-420e-a0a2-ce3f72c5cff4">FaxAccountSet</a>



<a href="https://msdn.microsoft.com/b4733772-92cb-4f4a-8a73-da1812356c30">IFaxAccountSet</a>
 

 

