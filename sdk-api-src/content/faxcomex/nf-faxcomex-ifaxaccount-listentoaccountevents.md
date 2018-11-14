---
UID: NF:faxcomex.IFaxAccount.ListenToAccountEvents
title: IFaxAccount::ListenToAccountEvents
author: windows-sdk-content
description: Sets the flags of a FAX_ACCOUNT_EVENTS_TYPE_ENUM variable that represents the events for which the account is listening.
old-location: fax\_mfax_faxaccount_cpp_mfax_faxaccount_listentoaccountevents_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccount\listentoaccountevents.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxAccount interface [Fax Service],ListenToAccountEvents method, IFaxAccount.ListenToAccountEvents, IFaxAccount::ListenToAccountEvents, ListenToAccountEvents, ListenToAccountEvents method [Fax Service], ListenToAccountEvents method [Fax Service],IFaxAccount interface, _mfax_faxaccount.listentoaccountevents, fax._mfax_faxaccount_cpp_mfax_faxaccount_listentoaccountevents_cpp, fax._mfax_faxaccount_listentoaccountevents, faxcomex/IFaxAccount::ListenToAccountEvents
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
 - IFaxAccount.ListenToAccountEvents
 - IFaxAccount.ListenToAccountEvents
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
- IFaxAccount.ListenToAccountEvents
: 
---

# IFaxAccount::ListenToAccountEvents


## -description


Sets the flags of a <a href="https://msdn.microsoft.com/1557462f-2686-42ea-b1a8-78fc86eefb68">FAX_ACCOUNT_EVENTS_TYPE_ENUM</a> variable that represents the events for which the account is listening.


## -parameters




### -param EventTypes [in]

Type: <b><a href="https://msdn.microsoft.com/1557462f-2686-42ea-b1a8-78fc86eefb68">FAX_ACCOUNT_EVENTS_TYPE_ENUM</a></b>

A variable that specifies the types of events for which the account is listening.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/85adc440-3dc8-47ce-aae8-dfb04f824b09">FaxAccount</a>



<a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a>
 

 

