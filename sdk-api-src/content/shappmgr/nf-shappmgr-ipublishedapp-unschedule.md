---
UID: NF:shappmgr.IPublishedApp.Unschedule
title: IPublishedApp::Unschedule (shappmgr.h)
author: windows-sdk-content
description: Cancels the installation of an application published by an application publisher.
old-location: shell\IPublishedApp_Unschedule.htm
tech.root: shell
ms.assetid: c0d5a8cb-d382-4d7a-8d09-2dd153c03294
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPublishedApp interface [Windows Shell],Unschedule method, IPublishedApp.Unschedule, IPublishedApp::Unschedule, Unschedule, Unschedule method [Windows Shell], Unschedule method [Windows Shell],IPublishedApp interface, inet_IPublishedApp_Unschedule, shappmgr/IPublishedApp::Unschedule, shell.IPublishedApp_Unschedule
ms.topic: method
f1_keywords: 
 - "shappmgr/IPublishedApp.Unschedule"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo">IPublishedApp::GetPublishedAppInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>
 

 

