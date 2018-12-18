---
UID: NF:faxcomex.IFaxIncomingArchive.GetMessages
title: IFaxIncomingArchive::GetMessages
author: windows-sdk-content
description: The GetMessages method returns a new iterator (archive cursor) for the archive of inbound fax messages.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1qnn.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],GetMessages method, IFaxIncomingArchive.GetMessages, IFaxIncomingArchive::GetMessages, _mfax_faxincomingarchive.getmessages, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessages_cpp, fax._mfax_faxincomingarchive_getmessages, faxcomex/IFaxIncomingArchive::GetMessages
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
 - IFaxIncomingArchive.GetMessages
 - IFaxIncomingArchive.GetMessages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingArchive::GetMessages


## -description


The <b>GetMessages</b> method returns a new iterator (archive cursor) for the archive of inbound fax messages.


## -parameters




### -param lPrefetchSize [in]

Type: <b>long</b>

<b>long</b> value that indicates the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms689196(v=VS.85).aspx">lDEFAULT_PREFETCH_SIZE</a>.


### -param pFaxIncomingMessageIterator [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms687519(v=VS.85).aspx">IFaxIncomingMessageIterator</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms687518(v=VS.85).aspx">FaxIncomingMessageIterator</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_IN_ARCHIVE</a> access right. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687473(v=VS.85).aspx">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687518(v=VS.85).aspx">FaxIncomingMessageIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687474(v=VS.85).aspx">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692976(v=VS.85).aspx">Visual Basic Example</a>
 

 

