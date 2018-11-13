---
UID: NF:faxcomex.IFaxAccountOutgoingArchive.GetMessages
title: IFaxAccountOutgoingArchive::GetMessages
author: windows-sdk-content
description: Returns a new iterator (archive cursor) for the archive of outbound fax messages for a particular fax account.
old-location: fax\_mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingarchive\getmessages.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxAccountOutgoingArchive interface, IFaxAccountOutgoingArchive interface [Fax Service],GetMessages method, IFaxAccountOutgoingArchive.GetMessages, IFaxAccountOutgoingArchive::GetMessages, _mfax_faxaccountoutgoingarchive.getmessages, fax._mfax_faxaccountoutgoingarchive_cpp_mfax_faxaccountoutgoingarchive_getmessages_cpp, fax._mfax_faxaccountoutgoingarchive_getmessages, faxcomex/IFaxAccountOutgoingArchive::GetMessages
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
 - IFaxAccountOutgoingArchive.GetMessages
 - IFaxAccountOutgoingArchive.GetMessages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountOutgoingArchive::GetMessages


## -description


Returns a new iterator (archive cursor) for the archive of outbound fax messages for a particular fax account.


## -parameters




### -param lPrefetchSize [in]

Type: <b>long</b>

<b>long</b> value that indicates the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="https://msdn.microsoft.com/447a730c-6033-46ab-9d90-0aad1aa4a429">lDEFAULT_PREFETCH_SIZE</a>.


### -param pFaxOutgoingMessageIterator

TBD




#### - pFaxOutgoingMessageIterator2 [out, retval]

Type: <b>IFaxOutgoingMessageIterator2**</b>

A <a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/21ed0cc8-23a3-4ac1-853f-8f7d004cf843">FaxAccountOutgoingArchive</a>



<a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a>



<a href="https://msdn.microsoft.com/cd2441ba-ed29-4ba5-b3f7-804fbca4d421">IFaxAccountOutgoingArchive</a>
 

 

