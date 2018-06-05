---
UID: NN:shobjidl.IUserAccountChangeCallback
title: IUserAccountChangeCallback
author: windows-sdk-content
description: Exposes a method which is called when the picture that represents a user account is changed.
old-location: shell\IUserAccountChangeCallback.htm
old-project: shell
ms.assetid: de72aa25-7d0c-445c-aa1b-f0f3bdc07d10
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUserAccountChangeCallback, IUserAccountChangeCallback interface [Windows Shell], IUserAccountChangeCallback interface [Windows Shell],described, _shell_IUserAccountChangeCallback, shell.IUserAccountChangeCallback, shobjidl/IUserAccountChangeCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	IUserAccountChangeCallback
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserAccountChangeCallback interface


## -description


Exposes a method which is called when the picture that represents a user account is changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserAccountChangeCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUserAccountChangeCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserAccountChangeCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e524edc-3921-4fec-9999-4fd9f51f347b">OnPictureChange</a>
</td>
<td align="left" width="63%">
Called to send notifications when the picture that represents a user account is changed.

</td>
</tr>
</table> 


## -remarks



Applications that want to notify users through this interface can add their class identifier (CLSID) strings as values under this key: 

                <pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>UserPictureChange</b></pre>


The values under this key are enumerated to create this callback object.



