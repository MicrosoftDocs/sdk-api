---
UID: NF:wuapi.IUpdateLockdown.LockDown
title: IUpdateLockdown::LockDown (wuapi.h)
author: windows-sdk-content
description: Restricts access to the methods and properties of the object that implements this method.
old-location: wua\iupdatelockdown_lockdown.htm
tech.root: Wua_Sdk
ms.assetid: 3d3be6f8-acdc-4cef-a0bc-6572a5b315d8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUpdateLockdown interface [Windows Update Agent],Lockdown method, IUpdateLockdown.LockDown, IUpdateLockdown::LockDown, IUpdateLockdown::Lockdown, LockDown, Lockdown method [Windows Update Agent], Lockdown method [Windows Update Agent],IUpdateLockdown interface, wua.iupdatelockdown_lockdown, wuapi/IUpdateLockdown::Lockdown
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateLockdown.Lockdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateLockdown::LockDown


## -description


Restricts access to the methods and properties of the object that implements this method.


## -parameters




### -param flags [in]

The option to restrict access to various Windows Update Agent (WUA) objects from the Windows Update website. 

Setting this parameter to  <b>uloForWebsiteAccess</b> or to 1 (one) restricts access to the WUA interfaces that implement the <a href="https://msdn.microsoft.com/918a46f5-a1da-4f47-84f1-b715fc97bb8f">IUpdateLockdown</a> interface.

For a list of the methods and properties that the WUA interfaces restrict when this value is specified, see the "Remarks" section.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The following table identifies the interfaces that implement the <a href="https://msdn.microsoft.com/918a46f5-a1da-4f47-84f1-b715fc97bb8f">IUpdateLockdown</a> interface.

<table>
<tr>
<th>WUA object</th>
<th>Restricted methods and properties</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d">IAutomaticUpdates</a>
</td>
<td>
<dl>
<dd>
<a href="https://msdn.microsoft.com/42985fdf-b3b3-43f0-addb-478298bd8ebd">Pause</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/8aabfb89-89e2-450e-bfe6-62a48f93746f">Resume</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a>
</td>
<td>
<dl>
<dd>
<a href="https://msdn.microsoft.com/fb54b900-345a-4b36-b16d-52790c0266f6">Save</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
</td>
<td>
<dl>
<dd>
<a href="https://msdn.microsoft.com/b3a25994-eace-45ec-8e6b-40d69796f168">AcceptEula</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/43af8bb9-0e09-4541-bc2e-fd40be64a980">CopyFromCache</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/a12f850a-df08-4263-bb66-94c45f7d875e">CopyToCache</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdateDownloader</a>
</td>
<td>
<dl>
<dd>
<a href="https://msdn.microsoft.com/8b860632-3d10-4791-b4b3-d37aad319a0a">BeginDownload</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">Download</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/b89ec12a-8a51-46e6-9911-2535abc3925b">EndDownload</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/e1ac3da4-341c-4a4e-920f-b84af03e324e">IsForced</a> (cannot set)</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
</td>
<td>
<dl>
<dd>
<a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">BeginInstall</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">BeginUninstall</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/7137164c-2b82-48dc-8488-6c8872896a39">EndInstall</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/a035f566-7ec6-41d5-b5b4-69c2acaa8aae">EndUninstall</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/009fc238-fcc4-4131-b770-9f0d0946e741">Install</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/80a30a21-9369-44bb-984a-2fdf2c1810e4">IsForced</a> (cannot set)</dd>
<dd>
<a href="https://msdn.microsoft.com/fd00fc89-077e-4897-a7ec-d2e06167b7b0">Uninstall</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/99b451b8-9831-475c-a4b0-7809f78d91b8">IUpdateServiceManager</a>
</td>
<td>
<dl>
<dd>
<a href="https://msdn.microsoft.com/5b0677bb-9f19-4bb4-9942-8ca3da18b29a">AddScanPackageService</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/fedd0979-1cc1-40c7-93d1-ade2f069ee76">RemoveService</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/dbf0b70c-5be0-4acc-9c44-bf32f6f752fd">SetOption</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/acc09635-7370-475f-9c3a-a5faaa8d576a">IWebProxy</a>
</td>
<td>
<dl>
<dd>
<a href="https://msdn.microsoft.com/ed8c899f-5080-435a-8577-7e92a54738ad">Address</a> (cannot set)</dd>
<dd>
<a href="https://msdn.microsoft.com/cd222133-e44b-453a-9fbf-72f609cb2d4b">AutoDetect</a> (cannot set)</dd>
<dd>
<a href="https://msdn.microsoft.com/a93742d2-73ce-4e7b-a000-592fd588cb1f">BypassList</a> (cannot set)</dd>
<dd>
<a href="https://msdn.microsoft.com/541626ca-0b68-41cd-8f20-5ffd034fc878">BypassProxyOnLocal</a> (cannot set)</dd>
<dd>
<a href="https://msdn.microsoft.com/59b500f1-2015-4f72-9be5-c2f57462dff0">SetPassword</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/cef38d9d-5706-4008-be61-5bbe7c29ca68">UserName</a> (cannot set)</dd>
</dl>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/918a46f5-a1da-4f47-84f1-b715fc97bb8f">IUpdateLockdown</a>
 

 

