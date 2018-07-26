---
UID: NF:faxcomex.IFaxServer.get_Folders
title: IFaxServer::get_Folders
author: windows-sdk-content
description: The Folders property accesses a FaxFolders configuration object. You can use the object to access the folders, jobs, and messages on a connected fax server.
old-location: fax\_mfax_faxserver_folders.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5ss3.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxServer object [Fax Service],Folders property, FaxServer.Folders, Folders property [Fax Service], Folders property [Fax Service],FaxServer object, IFaxServer.get_Folders, IFaxServer::get_Folders, _mfax_faxserver.folders, fax._mfax_faxserver_folders, get_Folders
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxServer.Folders
 - IFaxServer.get_Folders
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer::get_Folders


## -description


The <b>Folders</b> property accesses a <a href="https://msdn.microsoft.com/library/ms684837(v=VS.85).aspx">FaxFolders</a> configuration object. You can use the object to access the folders, jobs, and messages on a connected fax server. 

This property is read-only.


## -parameters


## -remarks



The folders that are accessible will depend on which privileges the user has. Users can always see their own inbound and outbound faxes. The tables below show what other faxes they can access depending on their privilege level.


<table class="clsStd">
<tr>
<th colspan="2">Windows Server 2003</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_IN_ARCHIVE</a>
</td>
<td>The user can view all fax messages in the incoming archive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farMANAGE_IN_ARCHIVE</a>
</td>
<td>The user can manage all fax messages in the incoming archive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_OUT_ARCHIVE</a>
</td>
<td>The user can view all fax messages in the outgoing archive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farMANAGE_OUT_ARCHIVE</a>
</td>
<td>The user can manage all fax messages in the outgoing archive.</td>
</tr>
</table>
 




<table class="clsStd">
<tr>
<th colspan="2">Windows Vista</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/Aa359062(v=VS.85).aspx">far2MANAGE_RECEIVE_FOLDER</a>
</td>
<td>The user can view and manage fax messages in the incoming archive that includes his own messages and unassigned messages.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_IN_ARCHIVE</a> or <a href="https://msdn.microsoft.com/library/Aa359062(v=VS.85).aspx">far2QUERY_ARCHIVES</a>
</td>
<td>The user can view all fax messages in the incoming archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farMANAGE_IN_ARCHIVE</a> or <a href="https://msdn.microsoft.com/library/Aa359062(v=VS.85).aspx">far2MANAGE_ARCHIVES</a>
</td>
<td>The user can manage all fax messages in the incoming archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_OUT_ARCHIVE</a> or <a href="https://msdn.microsoft.com/library/Aa359062(v=VS.85).aspx">far2QUERY_OUT_JOBS</a>
</td>
<td>The user can view all fax messages in the outgoing archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farMANAGE_OUT_ARCHIVE</a> or <a href="https://msdn.microsoft.com/library/Aa359062(v=VS.85).aspx">far2MANAGE_OUT_JOBS</a>
</td>
<td>The user can manage all fax messages in the outgoing archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/library/ms689110(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/library/ms692976(v=VS.85).aspx">Visual Basic Example</a>
 

 

