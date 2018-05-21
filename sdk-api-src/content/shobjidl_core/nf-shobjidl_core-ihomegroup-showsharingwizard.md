---
UID: NF:shobjidl_core.IHomeGroup.ShowSharingWizard
title: IHomeGroup::ShowSharingWizard
author: windows-driver-content
description: Displays a wizard that allows a user to create a Home Group, and then retrieves the sharing options that the user selected through the wizard.
old-location: shell\IHomeGroup_ShowSharingWizard.htm
old-project: shell
ms.assetid: D73A97EE-B427-4c53-B023-3662D864E801
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: HGSC_DOCUMENTSLIBRARY, HGSC_MUSICLIBRARY, HGSC_NONE, HGSC_PICTURESLIBRARY, HGSC_PRINTERS, HGSC_VIDEOSLIBRARY, IHomeGroup interface [Windows Shell],ShowSharingWizard method, IHomeGroup.ShowSharingWizard, IHomeGroup::ShowSharingWizard, ShowSharingWizard, ShowSharingWizard method [Windows Shell], ShowSharingWizard method [Windows Shell],IHomeGroup interface, _shell_IHomeGroup_ShowSharingWizard, shell.IHomeGroup_ShowSharingWizard, shobjidl_core/IHomeGroup::ShowSharingWizard
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IHomeGroup.ShowSharingWizard
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IHomeGroup::ShowSharingWizard


## -description


Displays a wizard that allows a user to create a Home Group, and then retrieves the sharing options that the user selected through the wizard.


## -parameters




### -param owner [in]

Type: <b>HWND</b>

Handle of the owner window of the wizard, used for notifications. This value can be <b>NULL</b>.


### -param sharingchoices [out]

Type: <b>HOMEGROUPSHARINGCHOICES*</b>

Pointer to a value that, when this method returns successfully, receives one or more of the following values that indicate the libraries and devices chosen through the wizard to be shared with the Home Group.



#### HGSC_NONE (0x00000000)

0x00000000. None of the Home Group options were selected



#### HGSC_MUSICLIBRARY (0x00000001)

0x00000001. The Music library was selected to be shared with the Home Group.



#### HGSC_PICTURESLIBRARY (0x00000002)

0x00000002. The Pictures library was selected to be shared with the Home Group..



#### HGSC_VIDEOSLIBRARY (0x00000004)

0x00000004. The Videos library was selected to be shared with the Home Group.



#### HGSC_DOCUMENTSLIBRARY (0x00000008)

0x00000008. The Documents library was selected to be shared with the Home Group.



#### HGSC_PRINTERS (0x00000010)

0x00000010. Installed printer devices were selected to be shared with the Home Group.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a standard error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the wizard. Use <a href="https://msdn.microsoft.com/40e6f80d-a778-4d5f-bb1b-db294815f8b5">HRESULT_FROM_WIN32</a> to extract this error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The computer is not joined to a Home Group or the network or Home Group is not in a state that allows sharing (such as not being connected to the network or having another sharing operation in progress).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The method was launched from a multithreaded apartment (MTA) thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>sharingchoices</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method must be called from a single-threaded apartment (STA) thread.


#### Examples

The following code shows an example use of <b>ShowSharingWizard</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
    IHomeGroup *phg;
    
    hr = CoCreateInstance(CLSID_HomeGroup, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&amp;phg));
    if (SUCCEEDED(hr))
    {
        HOMEGROUPSHARINGCHOICES sharingchoices;

        hr = phg-&gt;ShowSharingWizard(NULL, &amp;sharingchoices);
        if (SUCCEEDED(hr))
        {
            \\ The user selected to share.
            
            if (sharingchoices &amp; HGSC_MUSICLIBRARY)
            {
                \\ Music
            }
            if (sharingchoices &amp; HGSC_PICTURESLIBRARY)
            {
                \\ Pictures
            }
            if (sharingchoices &amp; HGSC_VIDEOSLIBRARY)
            {
                \\ Videos
            }
            if (sharingchoices &amp; HGSC_DOCUMENTSLIBRARY)
            {
                \\ Documents
            }
            if (sharingchoices &amp; HGSC_PRINTERS)
            {
                \\ Printers
            }
        }
        phg-&gt;Release();
    }
    CoUninitialize();
}</pre>
</td>
</tr>
</table></span></div>


