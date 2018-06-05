---
UID: NN:gpmgmt.IGPMAsyncProgress
title: IGPMAsyncProgress
author: windows-sdk-content
description: The IGPMAsyncProgress interface can be implemented by the client and passed as an input parameter to the Group Policy Management Console (GPMC) methods that can execute asynchronously.
old-location: gpmc\igpmasyncprogress.htm
old-project: GPMC
ms.assetid: f48b90db-5984-4ea7-826b-6fbbf3c33788
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IGPMAsyncProgress, IGPMAsyncProgress interface [GPMC], IGPMAsyncProgress interface [GPMC],described, _win32_igpmasyncprogress, gpmc.igpmasyncprogress, gpmgmt/IGPMAsyncProgress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMAsyncProgress
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMAsyncProgress interface


## -description


The <b>IGPMAsyncProgress</b> interface can be implemented by the client and passed as an 
    input parameter to the Group Policy Management Console (GPMC) methods that can execute asynchronously. The server 
    will then notify the client about the progress of the operation. Methods include 
    <a href="https://msdn.microsoft.com/19b3b027-59f1-4c31-896b-5b5fd23b9be4">IGPMGPO::GenerateReport</a>, 
    <a href="https://msdn.microsoft.com/d5daa512-547f-4b2d-85b3-0f6e9244acb2">IGPMBackup::GenerateReport</a>, 
    <a href="https://msdn.microsoft.com/86766a08-4f3a-4758-8abc-83db3408f0fd">IGPMRSOP::GenerateReport</a>, 
    <a href="https://msdn.microsoft.com/8e202ea1-ca5c-4757-950b-ea1802699b68">RestoreGPO</a>, 
    <a href="https://msdn.microsoft.com/5ba8d2f7-4989-4882-9ceb-4f77b8745442">Backup</a>, 
    <a href="https://msdn.microsoft.com/3b16eefb-89af-408b-a84c-c8ab958b4cc7">Import</a>, and 
    <a href="https://msdn.microsoft.com/17f4c6b2-6c75-4d4c-88c5-6d9ef2cb7a07">CopyTo</a>. This object cannot be accessed through scripting. 
    For more information, see the "Remarks" section.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMAsyncProgress</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMAsyncProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPMAsyncProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
</td>
<td align="left" width="63%">
The server calls this method to notify the client about the status of an asynchronous GPMC operation.

</td>
</tr>
</table> 


## -remarks



Complex GPMC operations, such as backup, restore, import, and copy operations, can execute asynchronously. To 
    use this interface with asynchronous operations, follow these steps.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To use this interface with asynchronous operations</b>

<ol>
<li>Implement the <b>IGPMAsyncProgress</b> interface.</li>
<li>Pass the <b>IGPMAsyncProgress</b> interface pointer to the GPMC method. For example, 
      pass the interface pointer to the 
      <a href="https://msdn.microsoft.com/8e202ea1-ca5c-4757-950b-ea1802699b68">RestoreGPO</a> method or to the 
      <a href="https://msdn.microsoft.com/3b16eefb-89af-408b-a84c-c8ab958b4cc7">Import</a> method.</li>
</ol>
The server will call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> method to 
    notify the client about the progress of the operation. This method also returns an 
    <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface pointer so that the caller can cancel the 
    operation by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a> method.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a>
 

 

