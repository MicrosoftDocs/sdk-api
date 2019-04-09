---
UID: NF:faxcomex.IFaxOutgoingArchive.GetMessages
title: IFaxOutgoingArchive::GetMessages (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingArchive::GetMessages method returns a new iterator (archive cursor) for the archive of outbound fax messages. For more information, see IFaxOutgoingMessageIterator.
old-location: fax\_mfax_faxoutgoingarchive_getmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_20qb_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMessages, GetMessages method [Fax Service], GetMessages method [Fax Service],IFaxOutgoingArchive interface, IFaxOutgoingArchive interface [Fax Service],GetMessages method, IFaxOutgoingArchive.GetMessages, IFaxOutgoingArchive::GetMessages, _mfax_faxoutgoingarchive.getmessages_cpp, fax._mfax_faxoutgoingarchive_getmessages_cpp, faxcomex/IFaxOutgoingArchive::GetMessages
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
 - IFaxOutgoingArchive.GetMessages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingArchive::GetMessages


## -description


The <b>IFaxOutgoingArchive::GetMessages</b> method returns a new iterator (archive cursor) for the archive of outbound fax messages. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690096(v=VS.85).aspx">IFaxOutgoingMessageIterator</a>.


## -parameters




### -param lPrefetchSize

Type: <b>long</b>

A <b>long</b> value that specifies the size of the prefetch buffer. This value determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms689196(v=VS.85).aspx">lDEFAULT_PREFETCH_SIZE</a>.


### -param pFaxOutgoingMessageIterator [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms690096(v=VS.85).aspx">IFaxOutgoingMessageIterator</a>**</b>

An address of a pointer that receives the <a href="https://msdn.microsoft.com/en-us/library/ms690096(v=VS.85).aspx">IFaxOutgoingMessageIterator</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <b>farQUERY_OUT_ARCHIVE</b> access right. With the <b>farSUBMIT_LOW</b> access right, the user will be able to use this method only for his own faxes. With the <b>farQUERY_OUT_ARCHIVE</b> access right, he will be able to use this method for all of the faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688636(v=VS.85).aspx">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693402(v=VS.85).aspx">Visual Basic Example</a>
 

 

