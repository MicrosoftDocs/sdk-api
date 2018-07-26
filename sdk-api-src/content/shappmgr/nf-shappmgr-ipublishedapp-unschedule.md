---
UID: NF:shappmgr.IPublishedApp.Unschedule
title: IPublishedApp::Unschedule
author: windows-sdk-content
description: Cancels the installation of an application published by an application publisher.
old-location: shell\IPublishedApp_Unschedule.htm
old-project: shell
ms.assetid: c0d5a8cb-d382-4d7a-8d09-2dd153c03294
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IPublishedApp interface [Windows Shell],Unschedule method, IPublishedApp.Unschedule, IPublishedApp::Unschedule, Unschedule, Unschedule method [Windows Shell], Unschedule method [Windows Shell],IPublishedApp interface, inet_IPublishedApp_Unschedule, shappmgr/IPublishedApp::Unschedule, shell.IPublishedApp_Unschedule
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PUBAPPINFOFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IPublishedApp.Unschedule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPublishedApp::Unschedule


## -description


Cancels the installation of an application published by an application publisher.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called in each of the following circumstances. 
				

<ol>
<li>The user selected the <b>Do Not Add Program</b> option in the <b>Add Later</b> dialog box in <b>Add/Remove Programs</b> in Control Panel.</li>
<li>The user has selected an installation time later than either the expiration time or the assigned time as specified in the published application information. In these circumstances, implementations are expected to cancel any scheduled installation for the application.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>



<a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a>



<a href="https://msdn.microsoft.com/2f56744c-a10e-423f-8b8f-c3257e560310">IShellApp</a>
 

 

