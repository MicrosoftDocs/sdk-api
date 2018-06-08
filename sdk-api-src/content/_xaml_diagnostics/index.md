---
UID: TP:xaml_diagnostics
ms.assetid: 9fd3de2c-6dbc-307e-b52e-afb4af9c54d0
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# XAML Diagnostics

## -description

Overview of the XAML Diagnostics technology.

To develop XAML Diagnostics, you need these headers:

 * [xamlom.h](../xamlom/index.md)

For the programming guide, see [XAML Diagnostics](/previous-versions/windows/desktop/xaml_diagnostics).

## Functions

| Title   | Description   |
| ---- |:---- |
| [InitializeXamlDiagnosticsEx function](..\xamlom\nf-xamlom-initializexamldiagnosticsex.md) | Initializes a Xaml Diagnostics session. This is the entry point for any debugging tool using the XAML Diagnostic APIs. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [BitmapDescription structure](..\xamlom\ns-xamlom-bitmapdescription.md) | Represents information about the bitmap stored in IBitmapData. |
| [CollectionElementValue structure](..\xamlom\ns-xamlom-collectionelementvalue.md) | Represents an element in a collection. |
| [EnumType structure](..\xamlom\ns-xamlom-enumtype.md) | Represents a XAML Runtime enumeration. |
| [ParentChildRelation structure](..\xamlom\ns-xamlom-parentchildrelation.md) | Associates a parent object with a child object. |
| [PropertyChainSource structure](..\xamlom\ns-xamlom-propertychainsource.md) | Represents the source object (a Style) of a target type. |
| [PropertyChainValue structure](..\xamlom\ns-xamlom-propertychainvalue.md) | Represents a property defined on an element. |
| [SourceInfo structure](..\xamlom\ns-xamlom-sourceinfo.md) | Represents information about an object’s XAML source document. |
| [VisualElement structure](..\xamlom\ns-xamlom-visualelement.md) | Represents a XAML element in the Live Visual Tree in Microsoft Visual Studio. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [BaseValueSource enumeration](..\xamlom\ne-xamlom-basevaluesource.md) | Defines constants that specify where the effective value of a property was set. |
| [MetadataBit enumeration](..\xamlom\ne-xamlom-metadatabit.md) | Defines constants that are used to define the PropertyChainValue returned from XAML Diagnostics. |
| [RenderTargetBitmapOptions enumeration](..\xamlom\ne-xamlom-rendertargetbitmapoptions.md) | Defines constants that specify what parts of the visual tree should be rendered. |
| [ResourceType enumeration](..\xamlom\ne-xamlom-resourcetype.md) | Defines constants that specify the type of a resource in a resource dictionary. |
| [VisualElementState enumeration](..\xamlom\ne-xamlom-visualelementstate.md) | Defines constants that specify the state of an element in the visual tree. |
| [VisualMutationType enumeration](..\xamlom\ne-xamlom-visualmutationtype.md) | Defines constants that specify whether the element was added to or removed from the live visual tree. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IBitmapData interface](..\xamlom\nn-xamlom-ibitmapdata.md) | Represents an image associated with a node in the visual tree. |
| [IVisualTreeService interface](..\xamlom\nn-xamlom-ivisualtreeservice.md) | Provides methods to manage a XAML visual tree. |
| [IVisualTreeService2 interface](..\xamlom\nn-xamlom-ivisualtreeservice2.md) | Represents additional capabilities of an IVisualTreeService object. |
| [IVisualTreeService3 interface](..\xamlom\nn-xamlom-ivisualtreeservice3.md) | Represents additional capabilities of an IVisualTreeService2 object. |
| [IVisualTreeServiceCallback interface](..\xamlom\nn-xamlom-ivisualtreeservicecallback.md) | Communicates the state of the visual tree. |
| [IVisualTreeServiceCallback2 interface](..\xamlom\nn-xamlom-ivisualtreeservicecallback2.md) | Represents additional capabilities of an IVisualTreeServiceCallback object. |
| [IXamlDiagnostics interface](..\xamlom\nn-xamlom-ixamldiagnostics.md) | Represents a XAML Diagnostics session. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IBitmapData::CopyBytesTo](..\xamlom\nf-xamlom-ibitmapdata-copybytesto.md) | Copies up to the specified maximum number of bytes from the given offset in the bitmap data into the caller’s buffer (pvBytes), and returns the number of bytes copied. |
| [IBitmapData::GetBitmapDescription](..\xamlom\nf-xamlom-ibitmapdata-getbitmapdescription.md) | Gets a BitmapDescription that describes the bitmap data stored in the IBitmapData. |
| [IBitmapData::GetSourceBitmapDescription](..\xamlom\nf-xamlom-ibitmapdata-getsourcebitmapdescription.md) | Gets a BitmapDescription that describes the original format of the bitmap data stored in the IBitmapData. |
| [IBitmapData::GetStride](..\xamlom\nf-xamlom-ibitmapdata-getstride.md) | Gets the stride of the data. This is the length in bytes of each row of the bitmap. |
| [IVisualTreeService3::AddDictionaryItem](..\xamlom\nf-xamlom-ivisualtreeservice3-adddictionaryitem.md) | Adds an item to a ResourceDictionary, and re-resolves all elements in the tree that reference a resource with the specified key. |
| [IVisualTreeService3::GetDictionaryItem](..\xamlom\nf-xamlom-ivisualtreeservice3-getdictionaryitem.md) | Gets an item from a ResourceDictionary. |
| [IVisualTreeService3::RemoveDictionaryItem](..\xamlom\nf-xamlom-ivisualtreeservice3-removedictionaryitem.md) | Removes an item from a ResourceDictionary, and re-resolves all elements in the tree that reference a resource with the specified key. |
| [IVisualTreeService3::ResolveResource](..\xamlom\nf-xamlom-ivisualtreeservice3-resolveresource.md) | Resolves a resource for an element in the tree and applies the resource to the property provided by the specified property index. |
| [IVisualTreeService::AddChild](..\xamlom\nf-xamlom-ivisualtreeservice-addchild.md) | Adds a child element to the collection at the specified index. |
| [IVisualTreeService::AdviseVisualTreeChange](..\xamlom\nf-xamlom-ivisualtreeservice-advisevisualtreechange.md) | Starts listening for changes to the visual tree. |
| [IVisualTreeService::ClearChildren](..\xamlom\nf-xamlom-ivisualtreeservice-clearchildren.md) | Clears all child elements from the parent collection. |
| [IVisualTreeService::ClearProperty](..\xamlom\nf-xamlom-ivisualtreeservice-clearproperty.md) | Clears the specified property on a XAML element. |
| [IVisualTreeService::CreateInstance](..\xamlom\nf-xamlom-ivisualtreeservice-createinstance.md) | Creates an instance of any XAML runtime, enum, or primitive type. |
| [IVisualTreeService::GetCollectionCount](..\xamlom\nf-xamlom-ivisualtreeservice-getcollectioncount.md) | Gets the count of a collection. |
| [IVisualTreeService::GetCollectionElements](..\xamlom\nf-xamlom-ivisualtreeservice-getcollectionelements.md) | Gets the elements in a collection. |
| [IVisualTreeService::GetEnums](..\xamlom\nf-xamlom-ivisualtreeservice-getenums.md) | Gets an array of all the enums defined in the XAML runtime and the total count. |
| [IVisualTreeService::GetPropertyValuesChain](..\xamlom\nf-xamlom-ivisualtreeservice-getpropertyvalueschain.md) | Gets an array of all the properties set on the element passed in, and an array of all the styles involved in setting the effective values of the properties. |
| [IVisualTreeService::RemoveChild](..\xamlom\nf-xamlom-ivisualtreeservice-removechild.md) | Removes the child element from the specified index. |
| [IVisualTreeService::SetProperty](..\xamlom\nf-xamlom-ivisualtreeservice-setproperty.md) | Sets a property value on a XAML element. |
| [IVisualTreeService::UnadviseVisualTreeChange](..\xamlom\nf-xamlom-ivisualtreeservice-unadvisevisualtreechange.md) | Stops listening for changes to the visual tree. |
| [IVisualTreeServiceCallback::OnVisualTreeChange](..\xamlom\nf-xamlom-ivisualtreeservicecallback-onvisualtreechange.md) | Communicates the state of the visual tree when it changes. |
| [IXamlDiagnostics::GetApplication](..\xamlom\nf-xamlom-ixamldiagnostics-getapplication.md) | Gets an instance of the application. |
| [IXamlDiagnostics::GetDispatcher](..\xamlom\nf-xamlom-ixamldiagnostics-getdispatcher.md) | Gets the core dispatcher used to access elements on the UI thread. |
| [IXamlDiagnostics::GetHandleFromIInspectable](..\xamlom\nf-xamlom-ixamldiagnostics-gethandlefromiinspectable.md) | Gets an InstanceHandle representation of an IInspectable. |
| [IXamlDiagnostics::GetIInspectableFromHandle](..\xamlom\nf-xamlom-ixamldiagnostics-getiinspectablefromhandle.md) | Gets the IInspectable from the XAML Diagnostics cache. |
| [IXamlDiagnostics::GetInitializationData](..\xamlom\nf-xamlom-ixamldiagnostics-getinitializationdata.md) | Gets the initialization data passed in to XAML Diagnostics. |
| [IXamlDiagnostics::GetUiLayer](..\xamlom\nf-xamlom-ixamldiagnostics-getuilayer.md) | Gets the visual diagnostics root that can be used to draw on for highlighting elements in the tree. |
| [IXamlDiagnostics::HitTest](..\xamlom\nf-xamlom-ixamldiagnostics-hittest.md) | Gets all elements in the visual tree that fall within the specified rectangle. |
| [IXamlDiagnostics::RegisterInstance](..\xamlom\nf-xamlom-ixamldiagnostics-registerinstance.md) | Adds an IInspectable to the XAML Diagnostics cache and returns the newly created InstanceHandle for the object. |
