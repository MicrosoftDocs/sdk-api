---
UID: NF:mobsync.ISyncMgrSynchronize.GetHandlerInfo
title: ISyncMgrSynchronize::GetHandlerInfo
author: windows-driver-content
description: Obtains handler information.
old-location: shell\syncmgr_isyncmgrsynchronize_gethandlerinfo.htm
old-project: shell
ms.assetid: bae3ead8-632c-45bf-a24e-bf07922039bd
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetHandlerInfo, GetHandlerInfo method [Windows Shell], GetHandlerInfo method [Windows Shell],ISyncMgrSynchronize interface, ISyncMgrSynchronize interface [Windows Shell],GetHandlerInfo method, ISyncMgrSynchronize.GetHandlerInfo, ISyncMgrSynchronize::GetHandlerInfo, mobsync/ISyncMgrSynchronize::GetHandlerInfo, shell.syncmgr_isyncmgrsynchronize_gethandlerinfo, syncmgr.isyncmgrsynchronize_gethandlerinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SYNCMGRSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mobsync.dll
api_name:
-	ISyncMgrSynchronize.GetHandlerInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronize::GetHandlerInfo


## -description


Obtains handler information.


## -parameters




### -param ppSyncMgrHandlerInfo [out]

Type: <b><a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a>**</b>

A pointer to a <a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a> structure.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Handler information is returned successfully.

</td>
</tr>
</table>
 




## -remarks



The handler should use the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function to allocate memory.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a>
 

 

