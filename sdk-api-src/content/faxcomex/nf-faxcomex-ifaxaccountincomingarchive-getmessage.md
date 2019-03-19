---
UID: NF:faxcomex.IFaxAccountIncomingArchive.GetMessage
title: IFaxAccountIncomingArchive::GetMessage (faxcomex.h)
author: windows-sdk-content
description: Returns a fax message from the archive of inbound faxes, for a particular fax account, by using the fax message ID.
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\getmessage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxAccountIncomingArchive interface, IFaxAccountIncomingArchive interface [Fax Service],GetMessage method, IFaxAccountIncomingArchive.GetMessage, IFaxAccountIncomingArchive::GetMessage, _mfax_faxaccountincomingarchive.getmessage, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_getmessage_cpp, fax._mfax_faxaccountincomingarchive_getmessage, faxcomex/IFaxAccountIncomingArchive::GetMessage
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
 - IFaxAccountIncomingArchive.GetMessage
 - IFaxAccountIncomingArchive.GetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountIncomingArchive::GetMessage


## -description


Returns a fax message from the archive of inbound faxes, for a particular fax account, by using the fax message ID.


## -parameters




### -param bstrMessageId [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of inbound faxes.


### -param pFaxIncomingMessage

TBD




#### - pFaxIncomingMessage2 [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>**</b>

An <a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2QUERY_ARCHIVES</a> access right. 

If the setting 'All incoming faxes are viewable by everyone' is true (see <a href="https://msdn.microsoft.com/en-us/library/Aa358923(v=VS.85).aspx">IncomingFaxesArePublic</a>) or if <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the fax service searches all faxes in the Incoming archive of the Fax Server Receive Folder.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358957(v=VS.85).aspx">FaxAccountIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359046(v=VS.85).aspx">IFaxAccountIncomingArchive</a>
 

 

