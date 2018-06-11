---
UID: NN:gpmgmt.IGPM2
title: IGPM2
author: windows-sdk-content
description: The IGPM2 interface extends the GPMBackupDir and InitializeReporting methods of the IGPM interface of the Group Policy Management Console (GPMC).
old-location: gpmc\igpm2.htm
old-project: GPMC
ms.assetid: f9cd432a-3974-4fc4-9e32-1d8e2df1601c
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IGPM2, IGPM2 interface [GPMC], IGPM2 interface [GPMC],described, gpmc.igpm2, gpmgmt/IGPM2
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPM2
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM2 interface


## -description


The 
<b>IGPM2</b> interface extends the <a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">GPMBackupDir</a> and <a href="https://msdn.microsoft.com/6e9f6ac5-d6d7-4360-b722-0b22e2391d20">InitializeReporting</a> methods of the <a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a> interface of the Group Policy Management Console (GPMC).

The <b>GPM</b> object is the only object used with 
the <a href="_com_cocreateinstance">CoCreateInstance</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPM2</b> interface inherits from <a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>. <b>IGPM2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPM2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fe4ea93-6668-4534-b72e-71b1062db627">GetBackupDirEx</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">GPMBackupDir</a> object which you can use to access 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> and  
<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">GPMBackupCollection</a> objects or <a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">GPMStarterGPOBackup</a> and  
<a href="https://msdn.microsoft.com/df9f29d0-8636-4393-8f7e-c9e22f3692f5">GPMStarterGPOBackupCollection</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3de74745-d9b3-47a7-8ba7-08b4e57d2ab7">InitializeReportingEx</a>
</td>
<td align="left" width="63%">
Sets the location of the .adm files specified by user and initiates reporting with options.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a02e9261-8bf5-4e1e-ae3f-64a763f93751">GPMC Interfaces</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>
 

 

