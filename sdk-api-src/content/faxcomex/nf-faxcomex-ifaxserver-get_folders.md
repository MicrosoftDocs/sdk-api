---
UID: NF:faxcomex.IFaxServer.get_Folders
title: IFaxServer::get_Folders
author: windows-sdk-content
description: The Folders property accesses a FaxFolders configuration object. You can use the object to access the folders, jobs, and messages on a connected fax server.
old-location: fax\_mfax_faxserver_folders.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5ss3.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
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


The <b>Folders</b> property accesses a <a href="https://msdn.microsoft.com/283c75e3-e596-403c-b4ea-b62bf0c744f3">FaxFolders</a> configuration object. You can use the object to access the folders, jobs, and messages on a connected fax server. 

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
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a>
</td>
<td>The user can view all fax messages in the incoming archive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_IN_ARCHIVE</a>
</td>
<td>The user can manage all fax messages in the incoming archive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_OUT_ARCHIVE</a>
</td>
<td>The user can view all fax messages in the outgoing archive.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_OUT_ARCHIVE</a>
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
<a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_RECEIVE_FOLDER</a>
</td>
<td>The user can view and manage fax messages in the incoming archive that includes his own messages and unassigned messages.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a> or <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_ARCHIVES</a>
</td>
<td>The user can view all fax messages in the incoming archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_IN_ARCHIVE</a> or <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_ARCHIVES</a>
</td>
<td>The user can manage all fax messages in the incoming archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_OUT_ARCHIVE</a> or <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_OUT_JOBS</a>
</td>
<td>The user can view all fax messages in the outgoing archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_OUT_ARCHIVE</a> or <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_OUT_JOBS</a>
</td>
<td>The user can manage all fax messages in the outgoing archive, including his own messages, unassigned messages, and messages assigned to others.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

