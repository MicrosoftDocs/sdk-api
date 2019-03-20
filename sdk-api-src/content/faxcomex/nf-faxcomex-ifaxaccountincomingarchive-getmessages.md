---
UID: NF:faxcomex.IFaxAccountIncomingArchive.GetMessages
title: IFaxAccountIncomingArchive::GetMessages (faxcomex.h)
author: windows-sdk-content
description: Returns a new iterator (archive cursor) for the archive of inbound fax messages for a particular fax account.
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\getmessages.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxAccountIncomingArchive interface, IFaxAccountIncomingArchive interface [Fax Service],GetMessages method, IFaxAccountIncomingArchive.GetMessages, IFaxAccountIncomingArchive::GetMessages, _mfax_faxaccountincomingarchive.getmessages, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessages_cpp, fax._mfax_faxaccountincomingarchive_getmessages, faxcomex/IFaxAccountIncomingArchive::GetMessages
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

<b>long</b> value that indicates the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms689196(v=VS.85).aspx">lDEFAULT_PREFETCH_SIZE</a>.


### -param pFaxIncomingMessageIterator

TBD




#### - pFaxIncomingMessageIterator2 [out, retval]

Type: <b>IFaxIncomingMessageIterator2**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms687518(v=VS.85).aspx">FaxIncomingMessageIterator</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the setting 'All incoming faxes are viewable by everyone' is true (see <a href="https://msdn.microsoft.com/en-us/library/Aa358923(v=VS.85).aspx">IncomingFaxesArePublic</a>) or if <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the fax service enumerates all faxes in the Incoming archive of the Fax Server Receive Folder.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358957(v=VS.85).aspx">FaxAccountIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687518(v=VS.85).aspx">FaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359046(v=VS.85).aspx">IFaxAccountIncomingArchive</a>
 

 

