---
UID: NN:shobjidl_core.IAttachmentExecute
title: IAttachmentExecute (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that work with client applications to present a user environment that provides safe download and exchange of files through email and messaging attachments.
old-location: shell\IAttachmentExecute.htm
tech.root: shell
ms.assetid: 2ebc3197-aa28-446e-8452-8ff71764fa9d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute, IAttachmentExecute interface [Windows Shell], IAttachmentExecute interface [Windows Shell],described, _win32_IAttachmentExecute, shell.IAttachmentExecute, shobjidl_core/IAttachmentExecute
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IAttachmentExecute"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAttachmentExecute interface


## -description


Exposes methods that work with client applications to present a user environment that provides safe download and exchange of files through email and messaging attachments.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAttachmentExecute</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAttachmentExecute</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-checkpolicy">CheckPolicy</a>
</td>
<td align="left" width="63%">
Provides a Boolean test that can be used to make decisions based on the attachment's execution policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-clearclientstate">ClearClientState</a>
</td>
<td align="left" width="63%">
Removes any stored state that is based on the client's GUID. An example might be a setting based on a checked box that indicates a prompt should not be displayed again for a particular file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-execute">Execute</a>
</td>
<td align="left" width="63%">
Executes an action on an attachment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt">Prompt</a>
</td>
<td align="left" width="63%">
Presents a prompt UI to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-save">Save</a>
</td>
<td align="left" width="63%">
Saves the attachment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-savewithui">SaveWithUI</a>
</td>
<td align="left" width="63%">
Presents the user with explanatory error UI if the save action fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setclientguid">SetClientGuid</a>
</td>
<td align="left" width="63%">
Specifies and stores the GUID for the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setclienttitle">SetClientTitle</a>
</td>
<td align="left" width="63%">
Specifies and stores the title of the prompt window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setfilename">SetFileName</a>
</td>
<td align="left" width="63%">
Specifies and stores the proposed name of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">SetLocalPath</a>
</td>
<td align="left" width="63%">
Sets and stores the path to the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setreferrer">SetReferrer</a>
</td>
<td align="left" width="63%">
Sets the security zone associated with the attachment file based on the referring file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setsource">SetSource</a>
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




