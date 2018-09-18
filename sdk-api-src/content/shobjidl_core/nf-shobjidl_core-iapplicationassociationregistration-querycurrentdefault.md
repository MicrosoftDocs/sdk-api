---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.QueryCurrentDefault
title: IApplicationAssociationRegistration::QueryCurrentDefault
author: windows-sdk-content
description: Determines the default application for a given association type. This is the default application launched by ShellExecute for that type. Not intended for use in Windows 8.
old-location: shell\IApplicationAssociationRegistration_QueryCurrentDefault.htm
tech.root: shell
ms.assetid: af6bd032-1457-4805-9844-87b5efb5ba21
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],QueryCurrentDefault method, IApplicationAssociationRegistration.QueryCurrentDefault, IApplicationAssociationRegistration::QueryCurrentDefault, QueryCurrentDefault, QueryCurrentDefault method [Windows Shell], QueryCurrentDefault method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_QueryCurrentDefault, shell.IApplicationAssociationRegistration_QueryCurrentDefault, shobjidl_core/IApplicationAssociationRegistration::QueryCurrentDefault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IApplicationAssociationRegistration.QueryCurrentDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationAssociationRegistration::QueryCurrentDefault


## -description


Determines the default application for a given association type. This is the default application launched by <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a> for that type. Not intended for use in Windows 8.


## -parameters




### -param pszQuery [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that contains the file name extension or protocol, such as .mp3 or http.


### -param atQueryType [in]

Type: <b><a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd">ASSOCIATIONTYPE</a></b>

One of the <a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd">ASSOCIATIONTYPE</a> enumeration values that specifies the type of association, such as extension or MIME type.


### -param alQueryLevel [in]

Type: <b><a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">ASSOCIATIONLEVEL</a></b>

One of the <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">ASSOCIATIONLEVEL</a> enumeration values that specifies the level of association, such as per-user or machine. This is typically <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">AL_EFFECTIVE</a>.


### -param ppszAssociation [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the ProgID that identifies the current default association.
                    

<div class="alert"><b>Note</b>  It is the responsibility of the calling application to release the string through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string produced is typically a ProgID matching one of the ProgIDs associated with a registered application, but there are a few exceptions: If the string returned is a machine default protocol, it is a legacy string indicating a command line to a .exe handler instead of a ProgID. Similarly, if returning a machine default MIME type, it returns a legacy class identifier (CLSID) string instead of a ProgID. 





## -see-also




<a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>



<a href="https://msdn.microsoft.com/015a3be4-2e74-4a2b-8c02-54dcbf0ecacd">IApplicationAssociationRegistration</a>
 

 

