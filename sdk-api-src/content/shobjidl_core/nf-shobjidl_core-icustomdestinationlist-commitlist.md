---
UID: NF:shobjidl_core.ICustomDestinationList.CommitList
title: ICustomDestinationList::CommitList
author: windows-sdk-content
description: Declares that the Jump List initiated by a call to ICustomDestinationList::BeginList is complete and ready for display.
old-location: shell\ICustomDestinationList_CommitList.htm
tech.root: shell
ms.assetid: 5f9aa598-9a94-4210-84cd-f4b39e47b260
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: CommitList, CommitList method [Windows Shell], CommitList method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],CommitList method, ICustomDestinationList.CommitList, ICustomDestinationList::CommitList, _shell_ICustomDestinationList_CommitList, shell.ICustomDestinationList_CommitList, shobjidl_core/ICustomDestinationList::CommitList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICustomDestinationList.CommitList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICustomDestinationList::CommitList


## -description


Declares that the Jump List initiated by a call to <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a> is complete and ready for display.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



As long as no call to <a href="https://msdn.microsoft.com/091a2b28-b4cf-46a9-845a-46b5aa86522d">AppendCategory</a> in this session failed for attempting to include a removed item, calling <b>CommitList</b> causes the stored list of removed items to be cleared and a new list of removed items to begin.




## -see-also




<a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a>



<a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

