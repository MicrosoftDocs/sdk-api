---
UID: NN:shobjidl_core.IAttachmentExecute
title: IAttachmentExecute
author: windows-sdk-content
description: Exposes methods that work with client applications to present a user environment that provides safe download and exchange of files through email and messaging attachments.
old-location: shell\IAttachmentExecute.htm
tech.root: shell
ms.assetid: 2ebc3197-aa28-446e-8452-8ff71764fa9d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IAttachmentExecute, IAttachmentExecute interface [Windows Shell], IAttachmentExecute interface [Windows Shell],described, _win32_IAttachmentExecute, shell.IAttachmentExecute, shobjidl_core/IAttachmentExecute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.dll: Shdocvw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IAttachmentExecute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAttachmentExecute interface


## -description


Exposes methods that work with client applications to present a user environment that provides safe download and exchange of files through email and messaging attachments.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAttachmentExecute</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAttachmentExecute</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAttachmentExecute</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff6a0aa8-4d14-4074-b084-be117b01c77a">CheckPolicy</a>
</td>
<td align="left" width="63%">
Provides a Boolean test that can be used to make decisions based on the attachment's execution policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/238e78be-3306-4ac5-95a9-c7fa48c1c4fe">ClearClientState</a>
</td>
<td align="left" width="63%">
Removes any stored state that is based on the client's GUID. An example might be a setting based on a checked box that indicates a prompt should not be displayed again for a particular file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80cbbb6c-c6f1-4937-9c1e-4de57aee748c">Execute</a>
</td>
<td align="left" width="63%">
Executes an action on an attachment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01c01abf-df7a-411b-979b-ddd8da569f91">Prompt</a>
</td>
<td align="left" width="63%">
Presents a prompt UI to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25661942-f38b-42d6-981b-4a3f4d083f6c">Save</a>
</td>
<td align="left" width="63%">
Saves the attachment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d5b2d02-98ee-4e46-826f-fa073ecff5c4">SaveWithUI</a>
</td>
<td align="left" width="63%">
Presents the user with explanatory error UI if the save action fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0ee35f7-c23e-450b-8b90-0fb5744263fd">SetClientGuid</a>
</td>
<td align="left" width="63%">
Specifies and stores the GUID for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24840acd-c2d1-43d8-99aa-8614e55d6604">SetClientTitle</a>
</td>
<td align="left" width="63%">
Specifies and stores the title of the prompt window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">SetFileName</a>
</td>
<td align="left" width="63%">
Specifies and stores the proposed name of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">SetLocalPath</a>
</td>
<td align="left" width="63%">
Sets and stores the path to the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7ee869a-2afe-4d98-a0bb-d80e57425079">SetReferrer</a>
</td>
<td align="left" width="63%">
Sets the security zone associated with the attachment file based on the referring file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6545252b-1c43-4d62-9784-b63688ef9fdc">SetSource</a>
</td>
<td align="left" width="63%">
Sets an alternate path or URL for the source of a file transfer.

</td>
</tr>
</table> 


## -remarks



This interface assumes the following:
                

<ul>
<li>The client has policies or settings  for attachment support and behavior.</li>
<li>The client interacts with the user.</li>
</ul>
The IID for this interface is <b>IID_IAttachmentExecute</b>.

Here is an example of how an email client might use <b>IAttachmentExecute</b>.



```

// CClientAttachmentInfo, defined by the client, implements all the
// necessary client functionality concerning attachments. 
class CClientAttachmentInfo;  

// Creates an instance of IAttachmentExecute
HRESULT CreateAttachmentServices(IAttachmentExecute **ppae)
{
    // Assume that CoInitialize has already been called for this thread.
    HRESULT hr = CoCreateInstance(CLSID_AttachmentServices, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_IAttachmentExecute, 
                                  (void**)&pAttachExec);

    if (SUCCEEDED(hr))
    {
        // Set the client's GUID.

        // UUID_ClientID should be created using uuidgen.exe and 
        // defined internally.
        (*ppae)->SetClientGuid(UUID_ClientID);
        
        // You also could call SetClientTitle at this point, but it is
        // not required.
    }
    return hr;
}

BOOL IsAttachmentBlocked(CClientAttachmentInfo *pinfo)
{
    // Assume that a client function has copied the file from the mail store 
    // into a temporary file.
    PWSTR pszFileName;

    // GetFileName is a method in this class for which we do not provide
    // an implementation here.
    HRESULT hr = pinfo->GetFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        IAttachmentExecute *pExecute;

        hr = CreateAttachmentServices(&pExecute);
        if (SUCCEEDED(hr))
        {
            hr = pExecute->SetFileName(pszFileName);

            // Do not call SetLocalPath since we do not have the local path yet.
            // Do not call SetSource since email sources are not verifiable.
            // Do not call SetReferrer since we do not have a better zone 
            // than the default (Restricted sites).

            // Check for a policy regarding the file.
            if (SUCCEEDED(hr))
            {
                hr = pExecute->CheckPolicy();
            }
            pExecute->Release();
        }
        LocalFree(pszFileName);
    }
    return FAILED(hr);
}
    
HRESULT OnDoubleClickAttachment(HWND hwnd, CClientAttachmentInfo *pinfo)
{
    // Assume that a client function has copied the file from the mail store 
    // into a temporary file.
    PWSTR pszTempFile;

    // CopyToTempFile is a method in this class for which we do not provide
    // an implementation here.
    HRESULT hr = pinfo->CopyToTempFile(&pszTempFile);
    if (SUCCEEDED(hr))
    {
        IAttachmentExecute *pExecute;

        hr = CreateAttachmentServices(&pExecute);
        if (SUCCEEDED(hr))
        {
            hr = pExecute->SetLocalPath(pszTempFile);

            // Do not call SetFileName since we already have the local path.
            // Do not call SetSource since email sources are not verifiable.
            // Do not call SetReferrer since we do not have a better zone 
            // than the default (Restricted sites).

            if (SUCCEEDED(hr))
            {
                hr = pExecute->Execute(hwnd, NULL, NULL);
            }
            pExecute->Release();
        }
        LocalFree(pszTempFile);
    }
    return hr;
}

HRESULT OnSaveAttachment(HWND hwnd, CClientAttachmentInfo *pinfo)
{
    // Assume that a client function has copied the file from the mail store 
    // into a location selected by the user.
    PWSTR pszUserFile;

    // CopyToUserFile is a method in this class for which we do not provide
    // an implementation here.
    HRESULT hr = pinfo->CopyToUserFile(hwnd, &pszUserFile);
    if (SUCCEEDED(hr))
    {
        IAttachmentExecute *pExecute;

        hr = CreateAttachmentServices(&pExecute);
        if (SUCCEEDED(hr))
        {
            hr = pExecute->SetLocalPath(pszTempFile);

            // Do not call SetFileName since we have the local path.
            // Do not call SetSource since email sources are not verifiable.
            // Do not call SetReferrer since we do not have a better zone 
            // than the default (Restricted sites).

            if (SUCCEEDED(hr))
            {
                hr = pExecute->Save();
            }
            pExecute->Release();
        }
        LocalFree(pszUserFile);
    }
    return hr;
}
```




