---
UID: NF:propsys.PSGetPropertyDescriptionByName
title: PSGetPropertyDescriptionByName function (propsys.h)
description: Gets an instance of a property description interface for a specified property name.
helpviewer_keywords: ["PSGetPropertyDescriptionByName","PSGetPropertyDescriptionByName function [Windows Properties]","properties.PSGetPropertyDescriptionByName","propsys/PSGetPropertyDescriptionByName","shell.PSGetPropertyDescriptionByName","shell_PSGetPropertyDescriptionByName"]
old-location: properties\PSGetPropertyDescriptionByName.htm
tech.root: properties
ms.assetid: 181ebbfb-66ed-4763-ad2d-acf3c800f9d2
ms.date: 12/05/2018
ms.keywords: PSGetPropertyDescriptionByName, PSGetPropertyDescriptionByName function [Windows Properties], properties.PSGetPropertyDescriptionByName, propsys/PSGetPropertyDescriptionByName, shell.PSGetPropertyDescriptionByName, shell_PSGetPropertyDescriptionByName
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSGetPropertyDescriptionByName
 - propsys/PSGetPropertyDescriptionByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetPropertyDescriptionByName
---

# PSGetPropertyDescriptionByName function


## -description

Gets an instance of a property description interface for a specified property name.

## -parameters

### -param pszCanonicalName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that identifies the property.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the interface ID of the requested property.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>, <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionaliasinfo">IPropertyDescriptionAliasInfo</a>, or  <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionsearchinfo">IPropertyDescriptionSearchInfo</a>.

## -returns

Type: <b>PSSTDAPI</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The interface was obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszCanonicalName</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The canonical name does not exist in the schema subsystem cache.

</td>
</tr>
</table>

## -remarks

 It is recommended that you use the IID_PPV_ARGS macro, defined in objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, eliminating the possibility of a coding error.

We recommend that <i>pszCanonicalName</i> point to the canonical name of a property, for example, <code>L"System.Keywords"</code>. The canonical name is case sensitive.

In addition to the new canonical names, callers can pass a legacy name for a property. The following table contains the complete list of supported legacy names and the canonical names they correspond to.

<table class="clsStd">
<tr>
<th>Property name</th>
<th>Maps to property</th>
</tr>
<tr>
<td>Access</td>
<td>System.DateAccessed</td>
</tr>
<tr>
<td>Album</td>
<td>System.Music.AlbumTitle</td>
</tr>
<tr>
<td>AllocSize</td>
<td>System.FileAllocationSize</td>
</tr>
<tr>
<td>Aperture</td>
<td>System.Photo.Aperture</td>
</tr>
<tr>
<td>Artist</td>
<td>System.Music.Artist</td>
</tr>
<tr>
<td>Attrib</td>
<td>System.FileAttributes</td>
</tr>
<tr>
<td>Attributes</td>
<td>System.FileAttributes</td>
</tr>
<tr>
<td>AttributesDescription</td>
<td>System.FileAttributesDisplay</td>
</tr>
<tr>
<td>Audio Format</td>
<td>System.Audio.Format</td>
</tr>
<tr>
<td>Audio Sample Size</td>
<td>System.Audio.SampleSize</td>
</tr>
<tr>
<td>BitDepth</td>
<td>System.Image.BitDepth</td>
</tr>
<tr>
<td>Bitrate</td>
<td>System.Audio.EncodingBitrate</td>
</tr>
<tr>
<td>CameraModel</td>
<td>System.Photo.CameraModel</td>
</tr>
<tr>
<td>Capacity</td>
<td>System.Capacity</td>
</tr>
<tr>
<td>Channels</td>
<td>System.Audio.ChannelCount</td>
</tr>
<tr>
<td>ColorSpace</td>
<td>System.Image.ColorSpace</td>
</tr>
<tr>
<td>Company</td>
<td>System.Company</td>
</tr>
<tr>
<td>Compression</td>
<td>System.Video.Compression</td>
</tr>
<tr>
<td>Compression</td>
<td>System.Video.Compression</td>
</tr>
<tr>
<td>Copyright</td>
<td>System.Copyright</td>
</tr>
<tr>
<td>Copyright</td>
<td>System.Copyright</td>
</tr>
<tr>
<td>Copyright</td>
<td>System.Image.Copyright</td>
</tr>
<tr>
<td>Create</td>
<td>System.DateCreated</td>
</tr>
<tr>
<td>CSCStatus</td>
<td>System.OfflineStatus</td>
</tr>
<tr>
<td>Data Rate</td>
<td>System.Video.EncodingBitrate</td>
</tr>
<tr>
<td>DateDeleted</td>
<td>System.Recycle.DateDeleted</td>
</tr>
<tr>
<td>DeletedFrom</td>
<td>System.Recycle.DeletedFrom</td>
</tr>
<tr>
<td>Dimensions</td>
<td>System.Image.Dimensions</td>
</tr>
<tr>
<td>Directory</td>
<td>System.ItemFolderNameDisplay</td>
</tr>
<tr>
<td>Distance</td>
<td>System.Photo.SubjectDistance</td>
</tr>
<tr>
<td>DocAppName</td>
<td>System.ApplicationName</td>
</tr>
<tr>
<td>DocAuthor</td>
<td>System.Author</td>
</tr>
<tr>
<td>DocByteCount</td>
<td>System.Document.ByteCount</td>
</tr>
<tr>
<td>DocCategory</td>
<td>System.Category</td>
</tr>
<tr>
<td>DocCharCount</td>
<td>System.Document.CharacterCount</td>
</tr>
<tr>
<td>DocComments</td>
<td>System.Comment</td>
</tr>
<tr>
<td>DocCompany</td>
<td>System.Company</td>
</tr>
<tr>
<td>DocCreatedTm</td>
<td>System.Document.DateCreated</td>
</tr>
<tr>
<td>DocEditTime</td>
<td>System.Document.TotalEditingTime</td>
</tr>
<tr>
<td>DocHiddenCount</td>
<td>System.Document.HiddenSlideCount</td>
</tr>
<tr>
<td>DocKeywords</td>
<td>System.Keywords</td>
</tr>
<tr>
<td>DocLastAuthor</td>
<td>System.Document.LastAuthor</td>
</tr>
<tr>
<td>DocLastPrinted</td>
<td>System.Document.DatePrinted</td>
</tr>
<tr>
<td>DocLastSavedTm</td>
<td>System.Document.DateSaved</td>
</tr>
<tr>
<td>DocLineCount</td>
<td>System.Document.LineCount</td>
</tr>
<tr>
<td>DocManager</td>
<td>System.Document.Manager</td>
</tr>
<tr>
<td>DocNoteCount</td>
<td>System.Document.NoteCount</td>
</tr>
<tr>
<td>DocPageCount</td>
<td>System.Document.PageCount</td>
</tr>
<tr>
<td>DocParaCount</td>
<td>System.Document.ParagraphCount</td>
</tr>
<tr>
<td>DocPresentationTarget</td>
<td>System.Document.PresentationFormat</td>
</tr>
<tr>
<td>DocRevNumber</td>
<td>System.Document.RevisionNumber</td>
</tr>
<tr>
<td>DocSlideCount</td>
<td>System.Document.SlideCount</td>
</tr>
<tr>
<td>DocSubject</td>
<td>System.Subject</td>
</tr>
<tr>
<td>DocTemplate</td>
<td>System.Document.Template</td>
</tr>
<tr>
<td>DocTitle</td>
<td>System.Title</td>
</tr>
<tr>
<td>DocWordCount</td>
<td>System.Document.WordCount</td>
</tr>
<tr>
<td>DRM Description</td>
<td>System.DRM.Description</td>
</tr>
<tr>
<td>Duration</td>
<td>System.Media.Duration</td>
</tr>
<tr>
<td>EquipMake</td>
<td>System.Photo.CameraManufacturer</td>
</tr>
<tr>
<td>ExposureBias</td>
<td>System.Photo.ExposureBias</td>
</tr>
<tr>
<td>ExposureProg</td>
<td>System.Photo.ExposureProgram</td>
</tr>
<tr>
<td>ExposureTime</td>
<td>System.Photo.ExposureTime</td>
</tr>
<tr>
<td>FaxCallerID</td>
<td>System.Fax.CallerID</td>
</tr>
<tr>
<td>FaxCSID</td>
<td>System.Fax.CSID</td>
</tr>
<tr>
<td>FaxRecipientName</td>
<td>System.Fax.RecipientName</td>
</tr>
<tr>
<td>FaxRecipientNumber</td>
<td>System.Fax.RecipientNumber</td>
</tr>
<tr>
<td>FaxRouting</td>
<td>System.Fax.Routing</td>
</tr>
<tr>
<td>FaxSenderName</td>
<td>System.Fax.SenderName</td>
</tr>
<tr>
<td>FaxTime</td>
<td>System.Fax.Time</td>
</tr>
<tr>
<td>FaxTSID</td>
<td>System.Fax.TSID</td>
</tr>
<tr>
<td>FileDescription</td>
<td>System.FileDescription</td>
</tr>
<tr>
<td>FileSystem</td>
<td>System.Volume.FileSystem</td>
</tr>
<tr>
<td>FileType</td>
<td>System.Image.FileType</td>
</tr>
<tr>
<td>FileVersion</td>
<td>System.FileVersion</td>
</tr>
<tr>
<td>Flash</td>
<td>System.Photo.Flash</td>
</tr>
<tr>
<td>FlashEnergy</td>
<td>System.Photo.FlashEnergy</td>
</tr>
<tr>
<td>FNumber</td>
<td>System.Photo.FNumber</td>
</tr>
<tr>
<td>FocalLength</td>
<td>System.Photo.FocalLength</td>
</tr>
<tr>
<td>Frame Rate</td>
<td>System.Video.FrameRate</td>
</tr>
<tr>
<td>FrameCount</td>
<td>System.Media.FrameCount</td>
</tr>
<tr>
<td>FreeSpace</td>
<td>System.FreeSpace</td>
</tr>
<tr>
<td>Genre</td>
<td>System.Music.Genre</td>
</tr>
<tr>
<td>ImageX</td>
<td>System.Image.HorizontalSize</td>
</tr>
<tr>
<td>ImageY</td>
<td>System.Image.VerticalSize</td>
</tr>
<tr>
<td>ISOSpeed</td>
<td>System.Photo.ISOSpeed</td>
</tr>
<tr>
<td>LightSource</td>
<td>System.Photo.LightSource</td>
</tr>
<tr>
<td>LinksUpToDate</td>
<td>System.Document.LinksDirty</td>
</tr>
<tr>
<td>LinkTarget</td>
<td>System.Link.TargetParsingPath</td>
</tr>
<tr>
<td>Lyrics</td>
<td>System.Music.Lyrics</td>
</tr>
<tr>
<td>Manager</td>
<td>System.Document.Manager</td>
</tr>
<tr>
<td>MeteringMode</td>
<td>System.Photo.MeteringMode</td>
</tr>
<tr>
<td>MMClipCount</td>
<td>System.Document.MultimediaClipCount</td>
</tr>
<tr>
<td>Name</td>
<td>System.ItemNameDisplay</td>
</tr>
<tr>
<td>Owner</td>
<td>System.FileOwner</td>
</tr>
<tr>
<td>Play Count</td>
<td>System.DRM.PlayCount</td>
</tr>
<tr>
<td>Play Expires</td>
<td>System.DRM.DatePlayExpires</td>
</tr>
<tr>
<td>Play Starts</td>
<td>System.DRM.DatePlayStarts</td>
</tr>
<tr>
<td>PresentationTarget</td>
<td>System.Document.PresentationFormat</td>
</tr>
<tr>
<td>ProductName</td>
<td>System.Software.ProductName</td>
</tr>
<tr>
<td>ProductVersion</td>
<td>System.Software.ProductVersion</td>
</tr>
<tr>
<td>Project</td>
<td>System.Media.Project</td>
</tr>
<tr>
<td>Protected</td>
<td>System.DRM.IsProtected</td>
</tr>
<tr>
<td>Rank</td>
<td>System.Search.Rank</td>
</tr>
<tr>
<td>Rating</td>
<td>System.Rating</td>
</tr>
<tr>
<td>ResolutionX</td>
<td>System.Image.HorizontalResolution</td>
</tr>
<tr>
<td>ResolutionY</td>
<td>System.Image.VerticalResolution</td>
</tr>
<tr>
<td>Sample Rate</td>
<td>System.Audio.SampleRate</td>
</tr>
<tr>
<td>Scale</td>
<td>System.Document.Scale</td>
</tr>
<tr>
<td>ShutterSpeed</td>
<td>System.Photo.ShutterSpeed</td>
</tr>
<tr>
<td>Size</td>
<td>System.Size</td>
</tr>
<tr>
<td>Software</td>
<td>System.SoftwareUsed</td>
</tr>
<tr>
<td>Status</td>
<td>System.Media.Status</td>
</tr>
<tr>
<td>Status</td>
<td>System.Status</td>
</tr>
<tr>
<td>Stream Name</td>
<td>System.Video.StreamName</td>
</tr>
<tr>
<td>SyncCopyIn</td>
<td>System.Sync.CopyIn</td>
</tr>
<tr>
<td>Track</td>
<td>System.Music.TrackNumber</td>
</tr>
<tr>
<td>Type</td>
<td>System.ItemTypeText</td>
</tr>
<tr>
<td>Video Sample Size</td>
<td>System.Video.SampleSize</td>
</tr>
<tr>
<td>WhenTaken</td>
<td>System.Photo.DateTaken</td>
</tr>
<tr>
<td>Write</td>
<td>System.DateModified</td>
</tr>
<tr>
<td>Year</td>
<td>System.Media.Year</td>
</tr>
</table>
 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionbyname">PSGetPropertyDescriptionByName</a> to retrieve the description for the ratings property.


```cpp
IPropertyDescription *pPropDesc;

HRESULT hr = PSGetPropertyDescriptionByName(L"System.Rating", IID_PPV_ARGS(&pPropDesc))

if (SUCCEEDED(hr))
{
    // pPropDesc is now valid.
 
    pPropDesc->Release();
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescription">PSGetPropertyDescription</a>