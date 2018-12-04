---
UID: NF:faxcomex.IFaxAccountSet.GetAccount
title: IFaxAccountSet::GetAccount
author: windows-sdk-content
description: Returns an IFaxAccount object by using the account name.
old-location: fax\_mfax_faxaccountset_cpp_mfax_faxaccountset_getaccount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\getaccount.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetAccount, GetAccount method [Fax Service], GetAccount method [Fax Service],IFaxAccountSet interface, IFaxAccountSet interface [Fax Service],GetAccount method, IFaxAccountSet.GetAccount, IFaxAccountSet::GetAccount, _mfax_faxaccountset.getaccount, fax._mfax_faxaccountset_cpp_mfax_faxaccountset_getaccount_cpp, fax._mfax_faxaccountset_getaccount, faxcomex/IFaxAccountSet::GetAccount
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
 - IFaxAccountSet.GetAccount
 - IFaxAccountSet.GetAccount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountSet::GetAccount


## -description


Returns an <a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a> object by using the account name.


## -parameters




### -param bstrAccountName [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the name of the account to return.


### -param pFaxAccount

TBD




#### - ppFaxAccount [out, retval]

Type: <b><a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<i>bstrAccountName</i> must be of the form &lt;domainName&gt;\&lt;username&gt; or just &lt;username&gt; for local users.




## -see-also




<a href="https://msdn.microsoft.com/ae298925-c428-420e-a0a2-ce3f72c5cff4">FaxAccountSet</a>



<a href="https://msdn.microsoft.com/b4733772-92cb-4f4a-8a73-da1812356c30">IFaxAccountSet</a>
 

 

