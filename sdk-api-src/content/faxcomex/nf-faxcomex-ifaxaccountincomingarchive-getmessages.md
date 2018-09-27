---
UID: NF:faxcomex.IFaxAccountIncomingArchive.GetMessages
title: IFaxAccountIncomingArchive::GetMessages
author: windows-sdk-content
description: Returns a new iterator (archive cursor) for the archive of inbound fax messages for a particular fax account.
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\getmessages.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxAccountIncomingArchive interface, IFaxAccountIncomingArchive interface [Fax Service],GetMessages method, IFaxAccountIncomingArchive.GetMessages, IFaxAccountIncomingArchive::GetMessages, _mfax_faxaccountincomingarchive.getmessages, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessages_cpp, fax._mfax_faxaccountincomingarchive_getmessages, faxcomex/IFaxAccountIncomingArchive::GetMessages
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
 - IFaxAccountIncomingArchive.GetMessages
 - IFaxAccountIncomingArchive.GetMessages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountIncomingArchive::GetMessages


## -description


Returns a new iterator (archive cursor) for the archive of inbound fax messages for a particular fax account.


## -parameters




### -param lPrefetchSize [in]

Type: <b>long</b>

<b>long</b> value that indicates the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="https://msdn.microsoft.com/447a730c-6033-46ab-9d90-0aad1aa4a429">lDEFAULT_PREFETCH_SIZE</a>.


### -param pFaxIncomingMessageIterator

TBD




#### - pFaxIncomingMessageIterator2 [out, retval]

Type: <b>IFaxIncomingMessageIterator2**</b>

A <a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the setting 'All incoming faxes are viewable by everyone' is true (see <a href="https://msdn.microsoft.com/f40268ab-6df0-4c4f-9c73-c3129be589cc">IncomingFaxesArePublic</a>) or if <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the fax service enumerates all faxes in the Incoming archive of the Fax Server Receive Folder.




## -see-also




<a href="https://msdn.microsoft.com/d2ae93a1-6325-4b8f-a227-4eb0678702d2">FaxAccountIncomingArchive</a>



<a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/8a10e18a-fed1-47b0-bb5b-b9f21f234c5b">IFaxAccountIncomingArchive</a>
 

 

