---
UID: NN:imapi2fs.IProgressItems
title: IProgressItems
author: windows-sdk-content
description: Use this interface to enumerate the progress items in a result image.
old-location: imapi\iprogressitems.htm
tech.root: imapi
ms.assetid: 40c28e67-8ff3-4330-90a1-7ebccb0023ad
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IProgressItems, IProgressItems interface [IMAPI], IProgressItems interface [IMAPI],described, imapi.iprogressitems, imapi2fs/IProgressItems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IProgressItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressItems interface


## -description


Use this interface to enumerate the progress items in a result image. A progress item represents a segment of the result image.

To get this interface, call the <a href="https://msdn.microsoft.com/c4ef572d-7e18-4537-847c-419441befe00">IFileSystemImageResult::get_ProgressItems</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProgressItems</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IProgressItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProgressItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24528fad-b88c-429a-b5c9-e232e62d3aeb">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves the list of progress items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/370386fe-17b0-4cf3-9c28-880a85456e19">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of progress items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/746b05b7-ddba-458c-bc9b-4913da5fa8b5">get_EnumProgressItems</a>
</td>
<td align="left" width="63%">
Retrieves the list of progress items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74d8e74d-0af6-457a-a16b-f959757b5a86">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified progress item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b37cf63-24be-42ff-a439-157703db9604">ProgressItemFromBlock</a>
</td>
<td align="left" width="63%">
Retrieves a progress item based on the specified block number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c27e9f30-e3f1-4436-b33a-fa3130baf374">ProgressItemFromDescription</a>
</td>
<td align="left" width="63%">
Retrieves a progress item based on the specified file name.

</td>
</tr>
</table> 


## -remarks



This is a <b>ProgressItems</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/c4238fbe-762a-492f-9eb5-d927e64436e1">IEnumProgressItems</a>



<a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a>
 

 

