---
UID: NF:shobjidl.IPublishingWizard.Initialize
title: IPublishingWizard::Initialize (shobjidl.h)
description: Initializes the Publishing Wizard object with the files to transfer, the settings to use, and the type of wizard to create.
helpviewer_keywords: ["AddNetPlace","IPublishingWizard interface [Windows Shell]","Initialize method","IPublishingWizard.Initialize","IPublishingWizard::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IPublishingWizard interface","InternetPhotoPrinting","SHPWHF_ANYLOCATION","SHPWHF_NOFILESELECTOR","SHPWHF_NONETPLACECREATE","SHPWHF_NORECOMPRESS","SHPWHF_USEMRU","SHPWHF_VALIDATEVIAWEBFOLDERS","_shell_IPublishingWizard_Initialize","shell.IPublishingWizard_Initialize","shobjidl/IPublishingWizard::Initialize"]
old-location: shell\IPublishingWizard_Initialize.htm
tech.root: shell
ms.assetid: 8312bb2e-cc06-4440-a72c-cf153a5d61b6
ms.date: 12/05/2018
ms.keywords: AddNetPlace, IPublishingWizard interface [Windows Shell],Initialize method, IPublishingWizard.Initialize, IPublishingWizard::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IPublishingWizard interface, InternetPhotoPrinting, SHPWHF_ANYLOCATION, SHPWHF_NOFILESELECTOR, SHPWHF_NONETPLACECREATE, SHPWHF_NORECOMPRESS, SHPWHF_USEMRU, SHPWHF_VALIDATEVIAWEBFOLDERS, _shell_IPublishingWizard_Initialize, shell.IPublishingWizard_Initialize, shobjidl/IPublishingWizard::Initialize
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Netplwiz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPublishingWizard::Initialize
 - shobjidl/IPublishingWizard::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netplwiz.dll
api_name:
 - IPublishingWizard.Initialize
---

# IPublishingWizard::Initialize


## -description

Initializes the <a href="/windows/desktop/shell/scriptable-shell-objects-roadmap">Publishing Wizard</a> object with the files to transfer, the settings to use, and the type of wizard to create.
			
            
<div class="alert"><b>Note</b>  Windows Vista no longer supports the Online Print Wizard. However, this method can still be used to generate the Add Network Place Wizard.</div><div> </div>

## -parameters

### -param pdo [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to an instance of <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> that represents the files or folder to be transferred, if <i>pszServiceProvider</i> is <code>InternetPhotoPrinting</code>. If <i>pszServiceProvider</i> is <code>AddNetPlace</code>, this parameter is <b>NULL</b>.

### -param dwOptions [in]

Type: <b>DWORD</b>

A combination of the following flags.



#### SHPWHF_NORECOMPRESS

Do not allow recompression of image data. For use with the Online Print Wizard.



#### SHPWHF_NONETPLACECREATE

Do not create a network place shortcut when the data transfer is complete. This flag is for use with the Add Network Place Wizard.



#### SHPWHF_NOFILESELECTOR

Do not allow the user to change the file selection within the wizard.



#### SHPWHF_USEMRU

Not supported.



#### SHPWHF_ANYLOCATION

<b>Windows Vista and later.</b> For use with the Add Network Place Wizard. If this flag is set, and <i>pszServiceProvider</i> is <code>AddNetPlace</code>, the Add Network Place wizard shows an option to select a network location other than the locations or providers that are registered to appear in the wizard.  



#### SHPWHF_VALIDATEVIAWEBFOLDERS

For use with the Add Network Place Wizard. In Windows XP, if this flag is set and an attempt to open the network location using WebDAV fails, the Add Network Place Wizard attempts to create a web folder for the location, using support for WEC. In Windows Vista and Windows Server 2003, this flag has no effect and network locations without support for WebDAV may not be opened as web folders.

### -param pszServiceScope [in]

Type: <b>LPCWSTR</b>

Unicode string that indicates the type of wizard to display. The following case-sensitive values are supported in Windows Vista.
				



#### AddNetPlace

Initialize the Add Network Place Wizard.



#### InternetPhotoPrinting

Initialize the Online Print Wizard. Not supported in Windows Vista.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
In Windows Vista, may indicate an attempt to initialize the unsupported Online Print Wizard by passing <code>InternetPhotoPrinting</code> in <i>pszServiceProvider</i>. 

                        

In Windows XP, may indicate that when initializing the Online Print Wizard, the <i>pdo</i> parameter is <b>NULL</b> or points to an empty selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszServiceProvider</i> parameter is not one of the supported values or the <i>dwOptions</i> parameter contains an unsupported combination of flags.

</td>
</tr>
</table>

## -remarks

<b>IPublishingWizard::Initialize</b>, implemented by a <a href="/windows/desktop/shell/scriptable-shell-objects-roadmap">Publishing Wizard</a> object, is called to initialize the wizard object.

The following sample does not work on Windows Vista because the Online Print Wizard cannot be instantiated through <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ipublishingwizard">IPublishingWizard</a> in Windows Vista.

				


```
/* initializing the Online Print Wizard in Windows XP or Windows 2003 Server*/
hr = pPublish->Initialize(pDataObject,  // A data object that represents files or 
                                        // folders to transfer.
                          SHPWHF_NOFILESELECTOR,     // Flags
                          L"InternetPhotoPrinting"); // Display the Online Print Wizard.
```


<b>IPublishingWizard::Initialize</b> does not actually display the initialized wizard. See the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ipublishingwizard">IPublishingWizard</a> topic for information on how to display the wizard.