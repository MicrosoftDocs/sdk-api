---
UID: NF:imapi2fs.IFileSystemImage.put_MultisessionInterfaces
title: IFileSystemImage::put_MultisessionInterfaces (imapi2fs.h)
description: Sets the list of multi-session interfaces for the optical media.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","put_MultisessionInterfaces method","IFileSystemImage.put_MultisessionInterfaces","IFileSystemImage::put_MultisessionInterfaces","imapi.ifilesystemimage_put_multisessioninterfaces","imapi2fs/IFileSystemImage::put_MultisessionInterfaces","put_MultisessionInterfaces","put_MultisessionInterfaces method [IMAPI]","put_MultisessionInterfaces method [IMAPI]","IFileSystemImage interface"]
old-location: imapi\ifilesystemimage_put_multisessioninterfaces.htm
tech.root: imapi
ms.assetid: 632cd123-4e66-4ac3-891a-aa9d0c085b4f
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_MultisessionInterfaces method, IFileSystemImage.put_MultisessionInterfaces, IFileSystemImage::put_MultisessionInterfaces, imapi.ifilesystemimage_put_multisessioninterfaces, imapi2fs/IFileSystemImage::put_MultisessionInterfaces, put_MultisessionInterfaces, put_MultisessionInterfaces method [IMAPI], put_MultisessionInterfaces method [IMAPI],IFileSystemImage interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemImage::put_MultisessionInterfaces
 - imapi2fs/IFileSystemImage::put_MultisessionInterfaces
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.put_MultisessionInterfaces
---

# IFileSystemImage::put_MultisessionInterfaces


## -description

Sets the list of multi-session interfaces for the optical media.

## -parameters

### -param newVal [in]

List of multi-session  interfaces for the optical media. Each element of the list is a VARIANT whose type is <b>VT_DISPATCH</b>. Query the multi-session interface for its <b>IDispatch</b> interface and set the <b>pdispVal</b> member of the variant to the <b>IDispatch</b> interface.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</b></dt>
</dl>
</td>
<td width="60%">
IMAPI does not support the multisession type requested.

Value: 0xC0AAB15B

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
IMAPI does not allow multi-session with the current media type.

Value: 0xC0AAB159

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</b></dt>
</dl>
</td>
<td width="60%">
IMAPI supports none of the multisession type(s) provided on the current media.

Value: 0xC0AAB15C

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BAD_MULTISESSION_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of multisession parameters cannot be retrieved or has a wrong value.

Value: 0xC0AAB162

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_FSI_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Internal error occurred: %1!ls!.


Value: 0xC0AAB100

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMPORT_SEEK_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Cannot seek to block %1!I64d! on source disc. This value is also returned if the optical media is blank.

Value: 0xC0AAB156

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Values returned by the  IUnknown::QueryInterface method may also be returned here.</div>
<div> </div>

## -remarks

This method validates that the multi-session type is compatible. The method succeeds if either

<ul>
<li>The list contains a single derived <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interface with <a href="/windows/desktop/api/imapi2/nf-imapi2-imultisession-put_inuse">IMultisession::put_InUse</a> set to VARIANT_TRUE and if the multi-session type is supported on the current media and supported by the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> implementation.</li>
<li>The list contains no derived <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interfaces whose <a href="/windows/desktop/api/imapi2/nf-imapi2-imultisession-put_inuse">IMultisession::put_InUse</a> property is set to VARIANT_TRUE, but contains at least one derived <b>IMultisession</b> that is supported on current media and supported by the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> implementation.</li>
</ul>
Unless the media is overwritable (i.e. DVD+/-RW, BD-RE, etc..), this method will fail if the media is blank. Failure will also occur if the list contains more than one <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interface whose <a href="/windows/desktop/api/imapi2/nf-imapi2-imultisession-put_inuse">IMultisession::put_InUse</a> property is set to VARIANT_TRUE, or no derived <b>IMultisession</b> interface is supported by the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> implementation. Currently, only the <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential">IMultisessionSequential</a> interface which derives from <b>IMultisession</b> is supported by <b>IFileSystemImage</b> implementation.

For an example, see <a href="/windows/desktop/imapi/creating-a-multisession-disc">Creating a Multisession Disc</a>.

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_multisessioninterfaces">IDiscFormat2Data::get_MultisessionInterfaces</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces">IFileSystemImage::get_MultisessionInterfaces</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>