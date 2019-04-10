---
UID: NF:msaatext.ICoCreatedLocally.LocalInit
title: ICoCreatedLocally::LocalInit (msaatext.h)
author: windows-sdk-content
description: Implemented by clients to return information about the local object.Note  Active Accessibility Text Services is deprecated.
old-location: winauto\icocreatedlocally_icocreatedlocally__localinit.htm
tech.root: WinAuto
ms.assetid: c2ad4462-4e8a-4f1f-8e44-b1494ca37399
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICoCreatedLocally interface [Windows Accessibility],LocalInit method, ICoCreatedLocally.LocalInit, ICoCreatedLocally::LocalInit, LocalInit, LocalInit method [Windows Accessibility], LocalInit method [Windows Accessibility],ICoCreatedLocally interface, _msaa_ICoCreatedLocally_LocalInit, msaa.icocreatedlocally_icocreatedlocally__localinit, msaatext/ICoCreatedLocally::LocalInit, winauto.icocreatedlocally_icocreatedlocally__localinit
ms.topic: method
req.header: msaatext.h
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
req.lib: 
req.dll: Msaatext.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - ICoCreatedLocally.LocalInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# ICoCreatedLocally::LocalInit


## -description


Implemented by clients to return information about the local object.<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="https://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		</div>
<div> </div>



## -parameters




### -param punkLocalObject [in]

Type: <b>IUnknown*</b>

A pointer to the server object.


### -param riidParam [in]

Type: <b>REFIID</b>

An optional interface parameter that is passed to the new helper object. This parameter specifies an interface identifier.


### -param punkParam [in]

Type: <b>IUnknown*</b>

An optional interface parameter that is passed to the new helper object. This parameter specifies the interface pointer.


### -param varParam [in]

Type: <b>VARIANT</b>

An optional interface parameter that is passed to the new helper object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.



